---
title: Satınalma sözleşmesi oluşturma
description: Bu yordam bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "338625"
---
# <a name="create-a-purchase-agreement"></a>Satınalma sözleşmesi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir. Bu genellikle bir satın alma yöneticisi tarafından yapılır. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce satınalma sözleşmesi sınıflandırmaları ayarlamış olmanız gerekir. Bir anlaşma oluşturduğunuzda bunu bir satınalma siparişi oluşturmak için kullanabilirsiniz ve bu satınalma sözleşmesinin koşulları, başlığa ve sözleşme tarafından etkilenen tüm sipariş satırlarına kopyalanır.


## <a name="create-a-new-purchase-agreement"></a>Yeni bir satınalma sözleşmesi oluşturun.
1. Tedarik ve kaynak Hizmeti > Satın alma anlaşmaları > Satın alma anlaşmaları seçeneğine git.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Satın alma sözleşmeleri sınıflandırması alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Genel bölümünü genişletin.
10. Bitiş tarihi alanına bir tarih girin.
    * Bu bitiş tarihi tüm taahhüt satırları için varsayılan olacaktır ve her bir taahhüdün ne kadar süreceğini belirleyecektir.  
11. Belge başlığı alanına satınalma sözleşmeniz için ad yazın.
    * Varsayılan taahhüt alanını Ürün miktarı taahhüdü olarak bırakın (veya bunun için ayarlanmamış ise buna çevirin).  
    * Varsayılan taahhüt değeri, sözleşme satırlarındaki seçeneklerinizi belirler. Sözleşme satırlarını oluştururken yeni bir taahhüt türüne ihtiyaç duyarsanız, başlıktaki varsayılan taahhütü değiştirmeniz gerekir.  4 tür taahhüt vardır. Ürün miktarı taahhüdü, belirli bir miktar ürün için. Ürün değeri taahhüdü, bir ürünün belirli bir para birimi tutarı için. Ürün kategori değeri taahhüdü: Bir tedarik kategorisindeki para birimi miktarı için, miktarın katalogda mevcut olan veya olmayan bir madde için. Değer taahhüdü, belirli bir para birimi miktarı için herhangi bir ürün veya herhangi bir tedarik kategorisi kullanılarak yerine getirilebilmek üzere.  
12. Tamam'a tıklayın.

## <a name="add-a-commitment"></a>Taahhüt ekleyin
1. Satır ekle'ye tıklayın.
2. Listede, seçili satırı işaretleyin.
3. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Bir taahhüt eklemek istediğiniz ürünü seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Miktar alanına bir sayı girin.
    * Bu, satıcınızdan satın almak üzere anlaştığınız toplam miktarıdır.  
7. Birim fiyatı alanına bir sayı girin.
8. Satır ayrıntıları bölümünü genişletin.
9. Maksimum uygulanır seçeneğini Evet olarak ayarlayın.
    * Maksimum zorlanan seçeneği, taahhüdün kullanımını sınırlar. Yalnızca satır için miktar alanında belirttiğiniz miktar kadar satın alabilirsiniz.  
10. Satır ayrıntıları bölümü daraltın.

## <a name="add-header-conditions"></a>Başlık koşulları ekleyin
1. Eylem Bölmesinde, Seçenekler'e tıklayın.
2. Görünümü değiştir'e tıklayın.
3. Başlık görünümü'ne tıklayın.
4. Koşullar bölümünü genişletin.
5. Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.
    * Satıcı hesabının ödeme koşulları burada varsayılan olarak gösterilir.       
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Teslimat şekli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Teslimat koşulları alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="confirm-and-activate-the-agreement"></a>Sözleşmeyi onaylayın ve etkinleştirin
1. Eylem Bölmesinde, Satınalma sözleşmesi'ne tıklayın.
2. Onay'a tıklayın
    * Anlaşmayı etkin olarak işaretle seçeneğini Evet olarak ayarlayın.  
3. Tamam'ı tıklatın.
4. Eylem Bölmesinde, Satınalma sözleşmesi'ne tıklayın.
5. Satınalma sözleşmesi onayları'nı tıklayın.
    * Önizleme/yazdırma seçeneği, bir belge yazdırmak veya satıcıya göndermek için bir satınalma anlaşması oluşturmanıza olanak sağlar. Daha sonra anlaşmayı günceller veya yeniden onaylarsanız, her iki sürüm de burada gösterilir.  
6. Sayfayı kapatın.

