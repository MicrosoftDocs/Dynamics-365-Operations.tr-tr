---
title: Servis Ürün Reçetesini Değiştirme
description: Servis Ürün Reçetesini Değiştirin.
author: ShylaThompson
manager: tfehr
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0c3656f765ea3c53c38679a1709a02fba36a848
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204242"
---
# <a name="modify-a-service-bom"></a><span data-ttu-id="b41ec-103">Servis Ürün Reçetesini Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b41ec-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b41ec-104">Servis ürün reçetesine bir öğenin geçmişini kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b41ec-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="b41ec-105">Bir ürün reçetesi satırını her güncelleştirdiğinizde, **Geçmiş** bölmesinde bir geçmiş satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b41ec-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="b41ec-106">Geçmiş satır ürün reçetesi satırının geçerli durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b41ec-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="b41ec-107">Servis ürün reçetesi öğesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b41ec-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="b41ec-108">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b41ec-109">**Servis sözleşmeleri** ayrıntılı formunu açmak için **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="b41ec-110">**Eylem Bölmesi** üzerinde **Servis nesneleri**'ne tıklayarak **Servis nesneleri** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="b41ec-111">Bir ürün reçetesi satırının güncelleştirileceği nesneyi seçin ve ardından **Tasarımcı**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="b41ec-112">**Tasarımcı** formunda, güncelleştirmek istediğiniz ürün reçetesi satırını seçin ve ardından **Ürün reçetesi satırını düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="b41ec-113"><STRONG>Kurulum</STRONG> sekmesinde, <STRONG>Ürün reçetesi satırı</STRONG> formunun bir satırı servis ürün reçetesine sürüklediğinizde açılmasını isterseniz <STRONG>Ekleme sırasında düzenle</STRONG> onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b41ec-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="b41ec-114">**Miktar** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="b41ec-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="b41ec-115">Yerine koyma maddesi için daha sonra faturalanabilecek bir servis siparişi satırı oluşturmak istiyorsanız **Servis siparişi satırı oluştur** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b41ec-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="b41ec-116">Formu kapatmak için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="b41ec-117">Servis ürün reçetesi satırını silme</span><span class="sxs-lookup"><span data-stu-id="b41ec-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="b41ec-118">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b41ec-119">**Servis sözleşmeleri** ayrıntılı formunu açmak için **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="b41ec-120">**Eylem Bölmesi** üzerinde **Servis nesneleri**'ne tıklayarak **Servis nesneleri** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="b41ec-121">Bir servis ürün reçetesi satırının silineceği nesneyi seçin ve ardından **Tasarımcı**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="b41ec-122">**Tasarımcı** formunda, silmek istediğiniz ürün reçetesi satırını seçin ve **Ürün reçetesi satırını sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b41ec-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b41ec-123">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b41ec-123">See also</span></span>

[<span data-ttu-id="b41ec-124">Şablon ürün reçeteleri</span><span class="sxs-lookup"><span data-stu-id="b41ec-124">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]