---
title: 在生产环境中运行组合和基于微服务的应用程序
description: 使用 Microsoft 平台和工具的容器化 Docker 应用程序的生命周期
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 18e6cb1fb5f496b66c89cb8e009a67894b8a76ad
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/06/2018
ms.locfileid: "48845291"
---
# <a name="run-composed-and-microservices-based-applications-in-production-environments"></a>在生产环境中运行组合和基于微服务的应用程序

由多个微服务构成的应用程序需要将部署到业务流程协调程序群集为了简化部署的复杂性和使其可行从 IT 角度来看。 没有与业务流程协调程序的群集，是很难部署和扩展的复杂微服务应用程序。

## <a name="introduction-to-orchestrators-schedulers-and-container-clusters"></a>业务流程协调程序、 计划程序，以及容器群集简介

前面的这本电子书，我们引入了*群集*并*计划程序*讨论有关软件体系结构和开发的一部分。 Docker 群集的示例包括 Docker Swarm 和 Mesosphere 的数据中心操作系统 (DC/OS)。 这两种可以提供由 Microsoft Azure 容器服务的基础结构的一部分运行。

当应用程序是向外扩展跨多个主机系统时，管理每个主机系统和抽象出底层平台的复杂性的能力变得极具吸引力。 这就准确地说是业务流程协调程序和计划程序提供的内容。 看看简要此处所示：

- **计划程序**。 "计划"是指管理员能够加载到建立如何运行特定容器的主机系统上的服务文件的功能。 启动 Docker 群集中的容器通常被称为计划。 尽管计划是指特定操作的加载服务定义中的，在更多常规意义上，计划程序负责挂接到主机的 init 系统中任何所需的容量管理服务。

   群集计划程序具有多个目标： 高效使用群集的资源中，使用用户提供的放置约束，计划具有的应用程序快速以不将它们保留在挂起状态，在一定程度"的公平性，"正在可靠的错误，并始终为可用。

- **业务流程**。 平台扩展到的主机群集中部署复杂的多容器工作负荷的生命周期管理功能。 通过将抽象化的主机基础结构，业务流程工具为用户提供了一种方法将整个群集视为单个部署目标。

   业务流程的过程包括工具和一个平台，可以自动从初始放置或部署每个容器; 应用程序管理的所有方面将容器移动到不同的主机，具体取决于其主机的运行状况或性能;版本控制和滚动更新和运行状况监视功能的支持缩放和故障转移;及更多。

   业务流程是一个泛指的术语，指容器计划、 群集管理和可能的预配其他主机。

提供的业务流程协调程序和计划程序的功能是非常复杂，若要开发和从零开始，创建，因此你通常会想要使用的业务流程解决方案提供的供应商。


>[!div class="step-by-step"]
[上一页](index.md)
[下一页](manage-production-docker-environments.md)
