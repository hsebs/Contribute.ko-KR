---
title: 중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로
description: 이 문서에서는 "중요한" 기여자 워크플로를 사용하여 docs.microsoft.com 문서에 참여하는 방법을 보여 줍니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: a43e9a8274c430b1eeed796fc74085c2248f1c14
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a><span data-ttu-id="7b43c-103">중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로</span><span class="sxs-lookup"><span data-stu-id="7b43c-103">GitHub contribution workflow for major or long-running changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b43c-104">docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 채택했습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="7b43c-105">자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="7b43c-106">또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="7b43c-107">공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="7b43c-108">변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="7b43c-109">끌어오기 요청을 병합하기 전에 온라인 양식을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-109">You will need to complete the online form before your pull request can be merged.</span></span>

## <a name="overview"></a><span data-ttu-id="7b43c-110">개요</span><span class="sxs-lookup"><span data-stu-id="7b43c-110">Overview</span></span>

<span data-ttu-id="7b43c-111">이 워크플로는 주요 변경 내용을 적용해야 하거나 리포지토리에 자주 참여할 참여자에게 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-111">This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository.</span></span> <span data-ttu-id="7b43c-112">자주 참여하는 사용자에게는 일반적으로 진행 중인(장기 실행) 변경 내용이 있습니다. 이 작업은 끌어오기 요청이 승인 및 병합되기 전에 여러 빌드/유효성 검사/스테이징 주기를 거치거나 여러 날에 걸쳐 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-112">Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.</span></span>

<span data-ttu-id="7b43c-113">공용 및 개인 리포지토리를 활용하는 프로젝트에서 작업하는 Microsoft 직원의 경우 개인 리포지토리에 이러한 방식으로 참여하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-113">For Microsoft employees who are working on projects that use both public and private repositories, it's also important to make these types of contributions to the private repository.</span></span> <span data-ttu-id="7b43c-114">통합된 OPS 빌드, 유효성 검사, 스테이징 서비스는 개인 리포지토리에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-114">Integrated OPS build, validation, and staging services are available in the private repository.</span></span>

<span data-ttu-id="7b43c-115">이러한 참여의 예제는 다음을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-115">Examples of these types of contributions include:</span></span>

[!INCLUDE[contribute-how-to-write-workflows-major-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a><span data-ttu-id="7b43c-116">용어</span><span class="sxs-lookup"><span data-stu-id="7b43c-116">Terminology</span></span>

<span data-ttu-id="7b43c-117">시작하기 전에 이 워크플로에서 사용되는 Git/GitHub 용어 및 monikers의 일부를 검토하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-117">Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow.</span></span> <span data-ttu-id="7b43c-118">이 내용을 이제 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-118">Don't worry about understanding them now.</span></span> <span data-ttu-id="7b43c-119">이 내용에 대해 배우게 됩니다. 정의를 확인해야 하는 경우 이 섹션을 다시 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-119">Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.</span></span>

| <span data-ttu-id="7b43c-120">이름</span><span class="sxs-lookup"><span data-stu-id="7b43c-120">Name</span></span> | <span data-ttu-id="7b43c-121">설명</span><span class="sxs-lookup"><span data-stu-id="7b43c-121">Description</span></span> |
|-----------|-------------|
|<span data-ttu-id="7b43c-122">포크</span><span class="sxs-lookup"><span data-stu-id="7b43c-122">fork</span></span>|<span data-ttu-id="7b43c-123">기본 GitHub 리포지토리의 복사본을 참조하는 경우 일반적으로 명사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-123">Normally used as a noun, when referring to a copy of a main GitHub repository.</span></span> <span data-ttu-id="7b43c-124">실제로 포크는 다른 리포지토리일 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-124">In practice, a fork is just another repository.</span></span> <span data-ttu-id="7b43c-125">하지만 GitHub이 기본/부모 리포지토리에 다시 연결된다는 점에서 구별됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-125">But it's special in the sense that GitHub maintains a connection back to the main/parent repository.</span></span> <span data-ttu-id="7b43c-126">"먼저 리포지토리를 포크해야 합니다."에서와 같이 동사로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-126">It's sometimes used as a verb, as in "You must fork the repository first."</span></span>|
|<span data-ttu-id="7b43c-127">원격</span><span class="sxs-lookup"><span data-stu-id="7b43c-127">remote</span></span>|<span data-ttu-id="7b43c-128">"원본" 또는 "업스트림" 원격과 같이 원격 리포지토리에 대한 명명된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-128">A named connection to a remote repository, such as the "origin" or "upstream" remote.</span></span> <span data-ttu-id="7b43c-129">이 연결은 다른 컴퓨터에서 호스팅되는 리포지토리를 참조하는 데 사용되므로 Git에서는 이 연결을 원격이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-129">Git refers to these as remotes because they are used to reference a repository that's hosted on another computer.</span></span> <span data-ttu-id="7b43c-130">이 워크플로에서 원격은 항상 GitHub 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-130">In this workflow, a remote is always a GitHub repository.</span></span>|
|<span data-ttu-id="7b43c-131">원본</span><span class="sxs-lookup"><span data-stu-id="7b43c-131">origin</span></span>|<span data-ttu-id="7b43c-132">로컬 리포지토리와 복제 원본 리포지토리 간 연결에 할당된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-132">The name assigned to the connection between your local repository and the repository from which it was cloned.</span></span> <span data-ttu-id="7b43c-133">이 워크플로에서 원본은 포크에 대한 연결을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-133">In this workflow, origin represents the connection to your fork.</span></span> <span data-ttu-id="7b43c-134">"변경 내용을 원본으로 푸시합니다."에서와 같이 원본 리포지토리 자체의 모니커로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-134">It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."</span></span>|
|<span data-ttu-id="7b43c-135">업스트림</span><span class="sxs-lookup"><span data-stu-id="7b43c-135">upstream</span></span>|<span data-ttu-id="7b43c-136">원본 원격과 같이 업스트림은 다른 리포지토리에 대한 명명된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-136">Like the origin remote, upstream is a named connection to another repository.</span></span> <span data-ttu-id="7b43c-137">이 워크플로에서 업스트림은 로컬 리포지토리와 포크를 만든 기본 리포지토리 간에 연결을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-137">In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created.</span></span> <span data-ttu-id="7b43c-138">"변경 내용을 업스트림으로 끌어옵니다."에서와 같이 업스트림 리포지토리 자체에 모니커로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-138">It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."</span></span>|

## <a name="workflow"></a><span data-ttu-id="7b43c-139">워크플로</span><span class="sxs-lookup"><span data-stu-id="7b43c-139">Workflow</span></span>

>[!IMPORTANT]
> <span data-ttu-id="7b43c-140">아직 [설정](get-started-setup-github.md) 단계를 완료하지 않은 경우 해당 단계를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-140">If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section.</span></span> <span data-ttu-id="7b43c-141">이 섹션은 GitHub 계정을 설정하고 Git Bash 및 Markdown 편집기를 설치하며 포크를 만들고 로컬 리포지토리를 설정하는 과정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-141">This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository.</span></span> <span data-ttu-id="7b43c-142">리포지토리 또는 분기와 같은 Git 및 GitHub 개념에 익숙하지 않은 경우 먼저 [Git 및 GitHub 기본 사항](git-github-fundamentals.md)을 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-142">If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).</span></span>

<span data-ttu-id="7b43c-143">이 워크플로에서 반복적인 주기에서 흐름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-143">In this workflow, changes flow in a repetitive cycle.</span></span> <span data-ttu-id="7b43c-144">장치의 로컬 리포지토리에서 시작하여 GitHub 포크로 이동하여 기본 GitHub 리포지토리로 이동한 다음 다른 참여자의 변경 내용을 포함하도록 다시 로컬로 돌아옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-144">Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.</span></span>

### <a name="use-github-flow"></a><span data-ttu-id="7b43c-145">GitHub Flow 사용</span><span class="sxs-lookup"><span data-stu-id="7b43c-145">Use GitHub flow</span></span>

<span data-ttu-id="7b43c-146">[Git 및 GitHub 기본 사항](git-github-fundamentals.md#git)에서 Git 리포지토리에는 마스터 분기와 마스터로 통합되지 않은 상태에서 진행 중인 추가 분기가 포함된다는 점을 상기하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-146">Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master.</span></span> <span data-ttu-id="7b43c-147">논리적으로 연결된 변경 내용 집합을 새로 지정할 때마다 워크플로를 통해 변경 내용을 관리하는 *작업 분기*를 만드는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-147">Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow.</span></span> <span data-ttu-id="7b43c-148">여기서 작업 분기라고 하는 이유는 변경 내용을 다시 마스터 분기로 통합하기 전까지 변경 내용을 반복/구체화하는 작업 영역이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-148">We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.</span></span>

<span data-ttu-id="7b43c-149">특정 분기에 연결된 변경 내용을 격리하면 해당 변경 내용을 독립적으로 제어하고 소개하고 게시 주기에 있는 특정 릴리스 시점에 대상으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-149">Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle.</span></span> <span data-ttu-id="7b43c-150">실제로, 작업 유형에 따라 리포지토리에 몇 개의 작업 분기를 쉽게 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-150">In reality, depending on the type of work you do, you can easily end up with several working branches in your repository.</span></span> <span data-ttu-id="7b43c-151">각각 다른 프로젝트를 나타내는 여러 분기에서 동시에 작업하는 것은 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-151">It's not uncommon to be working on multiple branches at the same time, each representing a different project.</span></span>

>[!TIP]
><span data-ttu-id="7b43c-152">마스터 분기에서 변경 내용을 지정하는 것은 적절하지 *않습니다*.</span><span class="sxs-lookup"><span data-stu-id="7b43c-152">Making your changes in the master branch is *not* a good practice.</span></span> <span data-ttu-id="7b43c-153">특정 시기에 기능을 릴리스하기 위해 마스터 분기를 사용하여 변경 내용을 적용하는 경우를 가정하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-153">Imagine that you use the master branch to introduce a set of changes for a timed feature release.</span></span> <span data-ttu-id="7b43c-154">변경 내용을 지정하고 릴리스되기를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-154">You finish the changes and are waiting to release them.</span></span> <span data-ttu-id="7b43c-155">그 사이에 어떤 문제를 해결해 달라는 긴급 요청을 받고 마스터 분기에 있는 파일을 변경한 다음 해당 변경 내용을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-155">Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change.</span></span> <span data-ttu-id="7b43c-156">이 예제에서는 특정 날짜에 릴리스하기 위해 유보하고 있던 수정 *및* 변경 내용을 의도치 않게 게시했습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-156">In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.</span></span>

<span data-ttu-id="7b43c-157">이제 로컬 리포지토리에서 새로운 작업 분기를 만들어 제안된 변경 내용을 캡처하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-157">Now let's create a new working branch in your local repository, to capture your proposed changes.</span></span> <span data-ttu-id="7b43c-158">Git 클라이언트는 각기 다르므로 원하는 클라이언트에 대한 도움말을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-158">Each git client is different, so consult the help for your preferred client.</span></span> <span data-ttu-id="7b43c-159">[GitHub Flow](https://guides.github.com/introduction/flow/)의 GitHub Guide에서 프로세스의 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-159">You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="7b43c-160">다음 단계</span><span class="sxs-lookup"><span data-stu-id="7b43c-160">Next steps</span></span>
<span data-ttu-id="7b43c-161">이것으로 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-161">That's it!</span></span> <span data-ttu-id="7b43c-162">여러분은 docs.microsoft.com 콘텐츠에 참여하셨습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43c-162">You've made a contribution to docs.microsoft.com content!</span></span>

- <span data-ttu-id="7b43c-163">Markdwon, Markdown 확장 구문과 같은 항목에 대해 자세히 알아보려면 계속해서 "필수 항목 작성" 섹션을 진행하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43c-163">To learn more about topics such as Markdown and Markdown extensions syntax, continue to the "Writing essentials" section.</span></span>