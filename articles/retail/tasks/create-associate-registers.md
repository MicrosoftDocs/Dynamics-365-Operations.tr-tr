--- 
title: " Kayıtlar oluşturma ve ilişkilendirme"
description: "Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1de4e71fd554ba0486a5d2f65803f0806df37fe4
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="393af-103"> Kayıtlar oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="393af-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="393af-104">Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="393af-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="393af-105">Bu yordam, USRT demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="393af-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="393af-106">Retail and commerce > Channel setup > POS setup > Registers (Perakende ve ticaret > Kanal kurulumu > POS kurulumu > Kayıtlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="393af-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="393af-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="393af-107">Click New.</span></span>
3. <span data-ttu-id="393af-108">Kayıt numarası alanında yeni kayıt için bir Kimlik yazın.</span><span class="sxs-lookup"><span data-stu-id="393af-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="393af-109">Kayıt kodu, genel olarak kaydın ait olduğu mağaza ve mağaza içindeki konum ile eşleşmesine yardımcı olan kodlar içerir.</span><span class="sxs-lookup"><span data-stu-id="393af-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="393af-110">Ad alanına kayıt için açıklayıcı bir ad yazın.</span><span class="sxs-lookup"><span data-stu-id="393af-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="393af-111">Mağaza numarası alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="393af-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="393af-112">Donanım profili alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="393af-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="393af-113">Donanım profilleri, yazar kasa çekmecesi ve fatura yazıcısı gibi kayıt cihazına bağlanacak perakende aksesuarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="393af-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="393af-114">Görsel profil alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="393af-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="393af-115">Sanal profiller, POS arka planında ve oturum açma sayfasında kullanılan görüntüleri belirlemek ve POS temaları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="393af-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="393af-116">EFT POS kayıt numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="393af-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="393af-117">EFT POS kayıt numarası, ödeme terminalinin yetkilendirme talepleri gönderdiği ödeme işlemcisini bilgilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="393af-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="393af-118">Bu değere genellikle "Terminal Kodu" veya “TID” adı verilir.</span><span class="sxs-lookup"><span data-stu-id="393af-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="393af-119">TID'yi genel olarak ödeme cihazının üzerinde bir etiket üzerinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="393af-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="393af-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="393af-120">Click Save.</span></span>


