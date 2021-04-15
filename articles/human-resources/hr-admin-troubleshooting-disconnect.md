---
title: İstemcisinin bağlantısı kesiliyor
description: Bu konu, müşteri ortamından bilinmediği sebeple bağlantısı kesilirse ne yapılacağını açıklar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9ec43ad0a7d121eb247d81d4b506556a0fa2214
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794913"
---
# <a name="client-disconnects"></a><span data-ttu-id="98e23-103">İstemcisinin bağlantısı kesiliyor</span><span class="sxs-lookup"><span data-stu-id="98e23-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="98e23-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="98e23-104">**Environment details**</span></span> 

<span data-ttu-id="98e23-105">Bu sorun her ortamda ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="98e23-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="98e23-106">**Belirti**</span><span class="sxs-lookup"><span data-stu-id="98e23-106">**Symptom**</span></span> 

<span data-ttu-id="98e23-107">Müşteri ortamından bilinmediği sebeple bağlantısı kesilirse.</span><span class="sxs-lookup"><span data-stu-id="98e23-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="98e23-108">Müşteri, aşağıdaki hata iletilerinden birini alır:</span><span class="sxs-lookup"><span data-stu-id="98e23-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="98e23-109">Bağlantınızı kaybettik.</span><span class="sxs-lookup"><span data-stu-id="98e23-109">We've lost your connection.</span></span> <span data-ttu-id="98e23-110">Çalışmaya devam etmek için Kapat'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98e23-110">Click Close to continue working.</span></span>
- <span data-ttu-id="98e23-111">Ağ bağlantınız kesilmiş olabilir, yeniden denemek için Yeniden Dene'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98e23-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="98e23-112">**Kırmızı bayrak**</span><span class="sxs-lookup"><span data-stu-id="98e23-112">**Red flag**</span></span>

<span data-ttu-id="98e23-113">Bu sorun genellikle kullanıcılar uygulama aşamasındayken, üretim ve test ortamları arasında bilgi kıyaslaması yaptıklarında ve oturumlar arası geçiş yaptıklarını unuttuklarında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="98e23-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="98e23-114">Kullanıcılar bu aşamadayken, büyük olasılıkla bu sorunla karşılaşacaklardır.</span><span class="sxs-lookup"><span data-stu-id="98e23-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="98e23-115">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="98e23-115">**Issue**</span></span> 

<span data-ttu-id="98e23-116">**Tarayıcı türleri:** Google Chrome, Internet Explorer ve Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="98e23-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="98e23-117">Microsoft Dynamics 365 Human Resources kullanıcılar aynı anda, aynı kullanıcı ve aynı tarayıcı türünden iki farklı oturum açtıklarında kullanıcıların bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="98e23-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="98e23-118">(Örneğin, kullanıcı A, hem ortam 1 hem de ortam 2'yi Chrome içerisinde görüntülüyor.) Kullanıcının farklı tarayıcı pencereleri veya sekmeler açması fark oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="98e23-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="98e23-119">Aynı kullanıcı kimlik bilgiler, hem ortam 1 hem de ortam 2 için aynı tarayıcı türünde aynı anda oturum açmakta kullanılırsa, İnsan Kaynakları oturumlardan birinin bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="98e23-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="98e23-120">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="98e23-120">**Solution**</span></span>

<span data-ttu-id="98e23-121">Bir tarayıcı türü için yalnızca bir ortamın açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="98e23-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="98e23-122">Kullanıcılar, aynı ortama birden fazla oturumu açabilirler (aynı tarayıcı içinde birden fazla sekmede).</span><span class="sxs-lookup"><span data-stu-id="98e23-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="98e23-123">İki ortam arasında aynı zamanda geçiş yapmak isteyen kullanıcılar, her bir ortamı farklı bir tarayıcı türünde açmalıdırlar.</span><span class="sxs-lookup"><span data-stu-id="98e23-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="98e23-124">(Örneğin, kullanıcı A ortam 1'i Chrome'da ve ortam 2'yi Microsoft Edge'de görüntüleyebilir.)</span><span class="sxs-lookup"><span data-stu-id="98e23-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]