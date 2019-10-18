---
title: Talent istemcisi bağlantısı kesiliyor
description: Bu konu, müşteri ortamından bilinmediği sebeple bağlantısı kesilirse ne yapılacağını açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008187"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="2b1b7-103">Talent istemcisi bağlantısı kesiliyor</span><span class="sxs-lookup"><span data-stu-id="2b1b7-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b1b7-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="2b1b7-104">**Environment details**</span></span> 

<span data-ttu-id="2b1b7-105">Bu sorun her ortamda ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="2b1b7-106">**Belirti**</span><span class="sxs-lookup"><span data-stu-id="2b1b7-106">**Symptom**</span></span> 

<span data-ttu-id="2b1b7-107">Müşteri ortamından bilinmediği sebeple bağlantısı kesilirse.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="2b1b7-108">Müşteri, aşağıdaki hata iletilerinden birini alır:</span><span class="sxs-lookup"><span data-stu-id="2b1b7-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="2b1b7-109">Bağlantınızı kaybettik.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-109">We've lost your connection.</span></span> <span data-ttu-id="2b1b7-110">Çalışmaya devam etmek için Kapat'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-110">Click Close to continue working.</span></span>
- <span data-ttu-id="2b1b7-111">Ağ bağlantınız kesilmiş olabilir, yeniden denemek için Yeniden Dene'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="2b1b7-112">**Kırmızı bayrak**</span><span class="sxs-lookup"><span data-stu-id="2b1b7-112">**Red flag**</span></span>

<span data-ttu-id="2b1b7-113">Bu sorun genellikle kullanıcılar uygulama aşamasındayken, üretim ve test ortamları arasında bilgi kıyaslaması yaptıklarında ve oturumlar arası geçiş yaptıklarını unuttuklarında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="2b1b7-114">Kullanıcılar bu aşamadayken, büyük olasılıkla bu sorunla karşılaşacaklardır.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="2b1b7-115">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="2b1b7-115">**Issue**</span></span> 

<span data-ttu-id="2b1b7-116">**Tarayıcı türleri:** Google Chrome, Internet Explorer ve Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2b1b7-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="2b1b7-117">Microsoft Dynamics 365 Talent kullanıcılar aynı anda, aynı kullanıcı ve aynı tarayıcı türünden iki farklı oturum açtıklarında kullanıcıların bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="2b1b7-118">(Örneğin, kullanıcı A, hem ortam 1 hem de ortam 2'yi Chrome içerisinde görüntülüyor.) Kullanıcının farklı tarayıcı pencereleri veya sekmeler açması fark oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="2b1b7-119">Aynı kullanıcı kimlik bilgiler, hem ortam 1 hem de ortam 2 için aynı tarayıcı türünde aynı anda oturum açmakta kullanılırsa, Talent oturumlardan birinin bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="2b1b7-120">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="2b1b7-120">**Solution**</span></span>

<span data-ttu-id="2b1b7-121">Bir tarayıcı türü için yalnızca bir ortamın açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="2b1b7-122">Kullanıcılar, aynı ortama birden fazla oturumu açabilirler (aynı tarayıcı içinde birden fazla sekmede).</span><span class="sxs-lookup"><span data-stu-id="2b1b7-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="2b1b7-123">İki ortam arasında aynı zamanda geçiş yapmak isteyen kullanıcılar, her bir ortamı farklı bir tarayıcı türünde açmalıdırlar.</span><span class="sxs-lookup"><span data-stu-id="2b1b7-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="2b1b7-124">(Örneğin, kullanıcı A ortam 1'i Chrome'da ve ortam 2'yi Microsoft Edge'de görüntüleyebilir.)</span><span class="sxs-lookup"><span data-stu-id="2b1b7-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
