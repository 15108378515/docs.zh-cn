---
title: "状态和 Docker 应用程序中的数据"
description: "为容器化的.NET 应用程序的.NET 微服务体系结构 |状态和 Docker 应用程序中的数据"
keywords: "Docker 微服务、 ASP.NET、 容器、 SQL、 CosmosDB、 Docker"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 36d0fb9f27ef56b36c380e2fc972c79cff77003e
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2017
---
# <a name="state-and-data-in-docker-applications"></a><span data-ttu-id="8d915-104">状态和 Docker 应用程序中的数据</span><span class="sxs-lookup"><span data-stu-id="8d915-104">State and data in Docker applications</span></span>

<span data-ttu-id="8d915-105">在大多数情况下，你可以将作为进程的实例的容器。</span><span class="sxs-lookup"><span data-stu-id="8d915-105">In most cases, you can think of a container as an instance of a process.</span></span> <span data-ttu-id="8d915-106">进程不维护持久状态。</span><span class="sxs-lookup"><span data-stu-id="8d915-106">A process does not maintain persistent state.</span></span> <span data-ttu-id="8d915-107">容器可以写入其本地存储，而假定，实例都将围绕无限期地将将如下假设将持久内存中的单个位置。</span><span class="sxs-lookup"><span data-stu-id="8d915-107">While a container can write to its local storage, assuming that an instance will be around indefinitely would be like assuming that a single location in memory will be durable.</span></span> <span data-ttu-id="8d915-108">应假定容器映像，如进程，拥有多个实例，或它们将最终终止;如果这些与容器 orchestrator 管理，它应假定，它们可能获取从一个节点或 VM 之间移动。</span><span class="sxs-lookup"><span data-stu-id="8d915-108">Container images, like processes, should be assumed to have multiple instances or that they will eventually be killed; if they’re managed with a container orchestrator, it should be assumed that they might get moved from one node or VM to another.</span></span>

<span data-ttu-id="8d915-109">Docker 提供了一个名为功能*覆盖文件系统*。</span><span class="sxs-lookup"><span data-stu-id="8d915-109">Docker provides a feature named the *overlay file system*.</span></span> <span data-ttu-id="8d915-110">这将实现存储到根文件系统容器的更新信息写入时复制任务。</span><span class="sxs-lookup"><span data-stu-id="8d915-110">This implements a copy-on-write task that stores updated information to the root file system of the container.</span></span> <span data-ttu-id="8d915-111">该信息是此外到容器所基于的原始映像中。</span><span class="sxs-lookup"><span data-stu-id="8d915-111">That information is in addition to the original image on which the container is based.</span></span> <span data-ttu-id="8d915-112">如果从系统中删除容器，这些更改将丢失。</span><span class="sxs-lookup"><span data-stu-id="8d915-112">If the container is deleted from the system, those changes are lost.</span></span> <span data-ttu-id="8d915-113">因此，虽然可能用于保存其本地存储中的容器的状态，但设计解决此系统与容器设计，它们的默认值是无状态的本地行冲突。</span><span class="sxs-lookup"><span data-stu-id="8d915-113">Therefore, while it is possible to save the state of a container within its local storage, designing a system around this would conflict with the premise of container design, which by default is stateless.</span></span>

<span data-ttu-id="8d915-114">以下解决方案用于管理 Docker 应用程序中的持久性数据：</span><span class="sxs-lookup"><span data-stu-id="8d915-114">The following solutions are used to manage persistent data in Docker applications:</span></span>

-   <span data-ttu-id="8d915-115">[数据卷](https://docs.docker.com/engine/tutorials/dockervolumes/)，装载到主机。</span><span class="sxs-lookup"><span data-stu-id="8d915-115">[Data volumes](https://docs.docker.com/engine/tutorials/dockervolumes/) that mount to the host.</span></span>

-   <span data-ttu-id="8d915-116">[数据卷容器](https://docs.docker.com/engine/tutorials/dockervolumes/#creating-and-mounting-a-data-volume-container)，在使用外部容器的容器内提供共享的存储。</span><span class="sxs-lookup"><span data-stu-id="8d915-116">[Data volume containers](https://docs.docker.com/engine/tutorials/dockervolumes/#creating-and-mounting-a-data-volume-container) that provide shared storage across containers using an external container.</span></span>

-   <span data-ttu-id="8d915-117">[卷插件](https://docs.docker.com/engine/tutorials/dockervolumes/)装载卷，向远程服务，并提供长期的持久性。</span><span class="sxs-lookup"><span data-stu-id="8d915-117">[Volume plugins](https://docs.docker.com/engine/tutorials/dockervolumes/) that mount volumes to remote services, providing long-term persistence.</span></span>

-   <span data-ttu-id="8d915-118">[Azure 存储](https://docs.microsoft.com/azure/storage/)，它提供可异地分发存储，为容器提供很好的长期持久性解决方案。</span><span class="sxs-lookup"><span data-stu-id="8d915-118">[Azure Storage](https://docs.microsoft.com/azure/storage/), which provides geo-distributable storage, providing a good long-term persistence solution for containers.</span></span>

-   <span data-ttu-id="8d915-119">远程关系数据库喜欢[Azure SQL 数据库](https://azure.microsoft.com/services/sql-database/)或 NoSQL 数据库，例如[Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction)，或缓存服务，如[Redis](https://redis.io/)。</span><span class="sxs-lookup"><span data-stu-id="8d915-119">Remote relational databases like [Azure SQL Database](https://azure.microsoft.com/services/sql-database/) or NoSQL databases like [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction), or cache services like [Redis](https://redis.io/).</span></span>

<span data-ttu-id="8d915-120">下面提供了有关这些选项的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="8d915-120">The following provides more detail about these options.</span></span>

<span data-ttu-id="8d915-121">**数据卷**的主机操作系统从映射到容器中的目录的目录。</span><span class="sxs-lookup"><span data-stu-id="8d915-121">**Data volumes** are directories mapped from the host OS to directories in containers.</span></span> <span data-ttu-id="8d915-122">当容器中的代码有权访问实际上是为主机操作系统上的目录的目录。</span><span class="sxs-lookup"><span data-stu-id="8d915-122">When code in the container has access to the directory, that access is actually to a directory on the host OS.</span></span> <span data-ttu-id="8d915-123">此目录不绑定到的容器本身的生存期和可以直接在主机操作系统上运行的代码访问目录或通过另一个容器，可以将相同的主机目录映射到其自身。</span><span class="sxs-lookup"><span data-stu-id="8d915-123">This directory is not tied to the lifetime of the container itself, and the directory can be accessed from code running directly on the host OS or by another container that maps the same host directory to itself.</span></span> <span data-ttu-id="8d915-124">因此，数据卷用于将独立于容器的生命周期的数据持久保存。</span><span class="sxs-lookup"><span data-stu-id="8d915-124">Thus, data volumes are designed to persist data independently of the life of the container.</span></span> <span data-ttu-id="8d915-125">如果删除容器，或将图像从 Docker 主机，数据保留在数据量不会删除。</span><span class="sxs-lookup"><span data-stu-id="8d915-125">If you delete a container or an image from the Docker host, the data persisted in the data volume is not deleted.</span></span> <span data-ttu-id="8d915-126">可以从主机操作系统以及访问在卷中的数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-126">The data in a volume can be accessed from the host OS as well.</span></span>

<span data-ttu-id="8d915-127">**数据卷容器**是演变而来的常规数据卷。</span><span class="sxs-lookup"><span data-stu-id="8d915-127">**Data volume containers** are an evolution of regular data volumes.</span></span> <span data-ttu-id="8d915-128">数据卷容器是具有在其中的一个或多个数据卷的简单容器。</span><span class="sxs-lookup"><span data-stu-id="8d915-128">A data volume container is a simple container that has one or more data volumes within it.</span></span> <span data-ttu-id="8d915-129">通过中央装入点还原时，数据卷容器提供对容器的访问。</span><span class="sxs-lookup"><span data-stu-id="8d915-129">The data volume container provides access to containers from a central mount point.</span></span> <span data-ttu-id="8d915-130">数据访问此方法是方便，因为它提取原始数据的位置。</span><span class="sxs-lookup"><span data-stu-id="8d915-130">This method of data access is convenient because it abstracts the location of the original data.</span></span> <span data-ttu-id="8d915-131">除此之外，其行为是类似于常规数据卷，其中，使数据保持独立应用程序的容器的生命周期于此专用容器中。</span><span class="sxs-lookup"><span data-stu-id="8d915-131">Other than that, its behavior is similar to that of a regular data volume, so data is persisted in this dedicated container independently of the lifecycle of the application’s containers.</span></span>

<span data-ttu-id="8d915-132">如所示在图 4-5 中，在容器本身之外，但主机服务器或 VM 的物理边界内，也可以存储正则 Docker 卷。</span><span class="sxs-lookup"><span data-stu-id="8d915-132">As shown in Figure 4-5, regular Docker volumes can be stored outside of the containers themselves but within the physical boundaries of the host server or VM.</span></span> <span data-ttu-id="8d915-133">但是，Docker 容器无法访问卷从一台主机服务器或 VM 到另一个。</span><span class="sxs-lookup"><span data-stu-id="8d915-133">However, Docker containers cannot access a volume from one host server or VM to another.</span></span> <span data-ttu-id="8d915-134">换而言之，使用这些卷，不能用于管理在不同的 Docker 主机运行的容器之间共享的数据</span><span class="sxs-lookup"><span data-stu-id="8d915-134">In other words, with these volumes, it is not possible to manage data shared between containers that run on different Docker hosts</span></span>

![](./media/image5.png)

<span data-ttu-id="8d915-135">**图 4-5**。</span><span class="sxs-lookup"><span data-stu-id="8d915-135">**Figure 4-5**.</span></span> <span data-ttu-id="8d915-136">数据卷和容器基于应用程序的外部数据源</span><span class="sxs-lookup"><span data-stu-id="8d915-136">Data volumes and external data sources for container-based applications</span></span>

<span data-ttu-id="8d915-137">此外，当通过 orchestrator 管理 Docker 容器时，容器可能""主机之间移动，具体取决于由群集执行的优化。</span><span class="sxs-lookup"><span data-stu-id="8d915-137">In addition, when Docker containers are managed by an orchestrator, containers might “move” between hosts, depending on the optimizations performed by the cluster.</span></span> <span data-ttu-id="8d915-138">因此，不建议你使用的数据卷业务数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-138">Therefore, it is not recommended that you use data volumes for business data.</span></span> <span data-ttu-id="8d915-139">但它们是一种良好的机制，可以使用跟踪文件、 临时文件、 或类似，不会影响业务数据一致性。</span><span class="sxs-lookup"><span data-stu-id="8d915-139">But they are a good mechanism to work with trace files, temporal files, or similar that will not impact business data consistency.</span></span>

<span data-ttu-id="8d915-140">**卷插件**如[Flocker](https://clusterhq.com/flocker/)跨群集中的所有主机提供数据访问。</span><span class="sxs-lookup"><span data-stu-id="8d915-140">**Volume plugins** like [Flocker](https://clusterhq.com/flocker/) provide data access across all hosts in a cluster.</span></span> <span data-ttu-id="8d915-141">而不是所有的卷插件都是相同的则卷插件通常提供外部化持久的可靠存储来自不可变的容器。</span><span class="sxs-lookup"><span data-stu-id="8d915-141">While not all volume plugins are created equally, volume plugins typically provide externalized persistent reliable storage from immutable containers.</span></span>

<span data-ttu-id="8d915-142">**远程数据源和缓存**工具，如 Azure SQL 数据库、 Azure Cosmos DB 或远程的缓存，如 Redis 可在容器应用程序相同的方式在没有容器的情况下开发时使用它们。</span><span class="sxs-lookup"><span data-stu-id="8d915-142">**Remote data sources and cache** tools like Azure SQL Database, Azure Cosmos DB, or a remote cache like Redis can be used in containerized applications the same way they are used when developing without containers.</span></span> <span data-ttu-id="8d915-143">这是一种经过验证的方式来存储业务应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-143">This is a proven way to store business application data.</span></span>

<span data-ttu-id="8d915-144">**Azure 存储空间。**</span><span class="sxs-lookup"><span data-stu-id="8d915-144">**Azure Storage.**</span></span> <span data-ttu-id="8d915-145">业务数据通常将需要放置外部资源或数据库，如 Azure 存储空间中。</span><span class="sxs-lookup"><span data-stu-id="8d915-145">Business data usually will need to be placed in external resources or databases, like Azure Storage.</span></span> <span data-ttu-id="8d915-146">具体中的 azure 存储提供了以下服务在云中：</span><span class="sxs-lookup"><span data-stu-id="8d915-146">Azure Storage, in concrete, provides the following services in the cloud:</span></span>

-   <span data-ttu-id="8d915-147">Blob 存储存储非结构化的对象数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-147">Blob storage stores unstructured object data.</span></span> <span data-ttu-id="8d915-148">Blob 可以是任何类型的文本或二进制数据，如文档或媒体文件 （图像、 音频和视频文件）。</span><span class="sxs-lookup"><span data-stu-id="8d915-148">A blob can be any type of text or binary data, such as document or media files (images, audio, and video files).</span></span> <span data-ttu-id="8d915-149">Blob 存储也称为对象存储。</span><span class="sxs-lookup"><span data-stu-id="8d915-149">Blob storage is also referred to as Object storage.</span></span>

-   <span data-ttu-id="8d915-150">文件存储为提供共享的存储使用标准 SMB 协议的旧版应用程序。</span><span class="sxs-lookup"><span data-stu-id="8d915-150">File storage offers shared storage for legacy applications using standard SMB protocol.</span></span> <span data-ttu-id="8d915-151">Azure 虚拟机和云服务可以在通过装载的共享的应用程序组件之间共享文件数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-151">Azure virtual machines and cloud services can share file data across application components via mounted shares.</span></span> <span data-ttu-id="8d915-152">在本地应用程序可以访问通过文件服务 REST API 的共享中的文件数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-152">On-premises applications can access file data in a share via the File service REST API.</span></span>

-   <span data-ttu-id="8d915-153">表存储存储结构化数据集。</span><span class="sxs-lookup"><span data-stu-id="8d915-153">Table storage stores structured datasets.</span></span> <span data-ttu-id="8d915-154">表存储是 NoSQL 键-属性数据存储，这将允许快速开发和快速访问大量数据。</span><span class="sxs-lookup"><span data-stu-id="8d915-154">Table storage is a NoSQL key-attribute data store, which allows rapid development and fast access to large quantities of data.</span></span>

<span data-ttu-id="8d915-155">**关系数据库和 NoSQL 数据库。**</span><span class="sxs-lookup"><span data-stu-id="8d915-155">**Relational databases and NoSQL databases.**</span></span> <span data-ttu-id="8d915-156">有多种可供选择的外部数据库，从关系数据库，如 SQL Server、 PostgreSQL、 Oracle 或 NoSQL 数据库，如 Azure Cosmos DB、 MongoDB 等。这些数据库不会被解释为本指南的一部分，因为它们在完全不同的使用者。</span><span class="sxs-lookup"><span data-stu-id="8d915-156">There are many choices for external databases, from relational databases like SQL Server, PostgreSQL, Oracle, or NoSQL databases like Azure Cosmos DB, MongoDB, etc. These databases are not going to be explained as part of this guide since they are in a completely different subject.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="8d915-157">[以前](化-整体-applications.md) [下一步] (服务-面向-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="8d915-157">[Previous] (containerize-monolithic-applications.md) [Next] (service-oriented-architecture.md)</span></span>