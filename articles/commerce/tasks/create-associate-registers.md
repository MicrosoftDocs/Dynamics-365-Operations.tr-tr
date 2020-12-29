---
title: " Kayıtlar oluşturma ve ilişkilendirme"
description: Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416485"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="b0d5f-103"> Kayıtlar oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="b0d5f-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0d5f-104">Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="b0d5f-105">Bu yordam, USRT demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="b0d5f-106">Retail and Commerce > Kanal kurulumu > POS kurulumu > Kayıtlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="b0d5f-107">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-107">Click New.</span></span>
3. <span data-ttu-id="b0d5f-108">Kayıt numarası alanında yeni kayıt için bir Kimlik yazın.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="b0d5f-109">Kayıt kodu, genel olarak kaydın ait olduğu mağaza ve mağaza içindeki konum ile eşleşmesine yardımcı olan kodlar içerir.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="b0d5f-110">Ad alanına kayıt için açıklayıcı bir ad yazın.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="b0d5f-111">Mağaza numarası alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="b0d5f-112">Donanım profili alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="b0d5f-113">Donanım profilleri, yazar kasa çekmecesi ve fatura yazıcısı gibi kayıt cihazına bağlanacak aksesuarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="b0d5f-114">Görsel profil alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="b0d5f-115">Sanal profiller, POS arka planında ve oturum açma sayfasında kullanılan görüntüleri belirlemek ve POS temaları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="b0d5f-116">EFT POS kayıt numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="b0d5f-117">EFT POS kayıt numarası, ödeme terminalinin yetkilendirme talepleri gönderdiği ödeme işlemcisini bilgilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="b0d5f-118">Bu değere genellikle "Terminal Kodu" veya “TID” adı verilir.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="b0d5f-119">TID'yi genel olarak ödeme cihazının üzerinde bir etiket üzerinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="b0d5f-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0d5f-120">Click Save.</span></span>

