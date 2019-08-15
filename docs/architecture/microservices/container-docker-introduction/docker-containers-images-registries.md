---
title: Docker 컨테이너, 이미지 및 레지스트리
description: 컨테이너화된 .NET 용용 프로그램용 .NET 마이크로 서비스 아키텍쳐 | Docker 컨테이너, 이미지 및 레지스트리
ms.date: 08/31/2018
ms.openlocfilehash: 520f8d4d54f1fdd227ff9a1e88660b62e75f927f
ms.sourcegitcommit: f20dd18dbcf2275513281f5d9ad7ece6a62644b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68674900"
---
# <a name="docker-containers-images-and-registries"></a><span data-ttu-id="2cce7-103">Docker 컨테이너, 이미지 및 레지스트리</span><span class="sxs-lookup"><span data-stu-id="2cce7-103">Docker containers, images, and registries</span></span>

<span data-ttu-id="2cce7-104">Docker를 사용할 때, 개발자는 앱 또는 서비스를 만들고 컨테이너 및 해당 종속성을 컨테이너 이미지에 패키지합니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-104">When using Docker, a developer creates an app or service and packages it and its dependencies into a container image.</span></span> <span data-ttu-id="2cce7-105">이미지는 앱 또는 서비스와 그 구성 및 종속성을 정적으로 표현합니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-105">An image is a static representation of the app or service and its configuration and dependencies.</span></span>

<span data-ttu-id="2cce7-106">앱 또는 서비스를 실행하려면 앱의 이미지가 인스턴스화되어 Docker 호스트에서 실행되는 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-106">To run the app or service, the app's image is instantiated to create a container, which will be running on the Docker host.</span></span> <span data-ttu-id="2cce7-107">컨테이너는 개발 환경 또는 PC에서 초기에 테스트됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-107">Containers are initially tested in a development environment or PC.</span></span>

<span data-ttu-id="2cce7-108">개발자는 이미지 라이브러리로 작동하는 레지스트리에 이미지를 저장해야 하며 프로덕션 오케스트레이터에 배포할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-108">Developers should store images in a registry, which acts as a library of images and is needed when deploying to production orchestrators.</span></span> <span data-ttu-id="2cce7-109">Docker는 [Docker 허브](https://hub.docker.com/)를 통해 공용 레지스트리를 관리합니다. 다른 공급업체는 다른 이미지 컬렉션을 위한 [Azure Container Registry](https://azure.microsoft.com/services/container-registry/) 등의 레지스트리를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-109">Docker maintains a public registry via [Docker Hub](https://hub.docker.com/); other vendors provide registries for different collections of images, including [Azure Container Registry](https://azure.microsoft.com/services/container-registry/).</span></span> <span data-ttu-id="2cce7-110">또는 기업에서는 자체 Docker 이미지를 위해 개인 레지스트리 온-프레미스를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-110">Alternatively, enterprises can have a private registry on-premises for their own Docker images.</span></span>

<span data-ttu-id="2cce7-111">그림 2-4는 Docker의 이미지와 레지스트리가 다른 구성 요소와 어떤 관계가 있는지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-111">Figure 2-4 shows how images and registries in Docker relate to other components.</span></span> <span data-ttu-id="2cce7-112">그것은 또한 공급업체로부터 제공되는 여러 레지스트리를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-112">It also shows the multiple registry offerings from vendors.</span></span>

![Docker의 기본 분류: 레지스트리는 이미지가 저장되고 컨테이너를 빌드하여 서비스 또는 웹앱을 실행하기 위해 가져올 수 있는 책장과 같습니다.](./media/image5.PNG)

<span data-ttu-id="2cce7-117">**그림 2-4**.</span><span class="sxs-lookup"><span data-stu-id="2cce7-117">**Figure 2-4**.</span></span> <span data-ttu-id="2cce7-118">Docker 용어 및 개념의 분류</span><span class="sxs-lookup"><span data-stu-id="2cce7-118">Taxonomy of Docker terms and concepts</span></span>

<span data-ttu-id="2cce7-119">레지스티리에 이미지를 저장하면 프레임워크 수준에서 모든 종속성을 포함하여 정적 및 변경할 수 없는 애플리케이션 비트를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-119">Putting images in a registry lets you store static and immutable application bits, including all their dependencies at a framework level.</span></span> <span data-ttu-id="2cce7-120">이러한 이미지는 여러 환경에서 버전을 지정하고 배포할 수 있으므로 일관된 배포 단위를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-120">Those images can then be versioned and deployed in multiple environments and therefore provide a consistent deployment unit.</span></span>

<span data-ttu-id="2cce7-121">온-프레미스 또는 클라우드에서 호스팅되는 개인 이미지 레지스티리는 다음과 같은 경우에 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-121">Private image registries, either hosted on-premises or in the cloud, are recommended when:</span></span>

- <span data-ttu-id="2cce7-122">기밀로 인해 이미지를 공개적으로 공유해서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-122">Your images must not be shared publicly due to confidentiality.</span></span>

- <span data-ttu-id="2cce7-123">이미지와 선택한 배포 환경 사이에는 최소 네트워크 대기 시간이 요구됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-123">You want to have minimum network latency between your images and your chosen deployment environment.</span></span> <span data-ttu-id="2cce7-124">예를 들어, 프로덕션 환경이 Azure 클라우드인 경우 [Azure Container Registry](https://azure.microsoft.com/services/container-registry/)에 이미지를 저장하여 네트워크 대기 시간을 최소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-124">For example, if your production environment is Azure cloud, you probably want to store your images in [Azure Container Registry](https://azure.microsoft.com/services/container-registry/) so that network latency will be minimal.</span></span> <span data-ttu-id="2cce7-125">프로덕션 환경이 동일한 로컬 네트워크 내에서 사용 가능한 온-프레미스 Docker Trusted Registry인 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="2cce7-125">In a similar way, if your production environment is on-premises, you might want to have an on-premises Docker Trusted Registry available within the same local network.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="2cce7-126">[이전](docker-terminology.md)
>[다음](../net-core-net-framework-containers/index.md)</span><span class="sxs-lookup"><span data-stu-id="2cce7-126">[Previous](docker-terminology.md)
[Next](../net-core-net-framework-containers/index.md)</span></span>