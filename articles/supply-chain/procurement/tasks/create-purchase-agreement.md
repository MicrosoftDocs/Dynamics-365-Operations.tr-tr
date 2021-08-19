---
title: Satınalma sözleşmesi oluşturma
description: Bu konu bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir.
author: kamaybac
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8085f5d30e1fbbc11b3bc4f86899a54615b039bb3e72fbeafb9bd74e87c1fbfa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717256"
---
# <a name="create-a-purchase-agreement"></a>Satınalma sözleşmesi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu bir satın alma sözleşmesi oluşturma aşamasında size yol gösterir. Bu genellikle bir satın alma yöneticisi tarafından yapılır. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce satınalma sözleşmesi sınıflandırmaları ayarlamış olmanız gerekir. Bir anlaşma oluşturduğunuzda bunu bir satınalma siparişi oluşturmak için kullanabilirsiniz ve bu satınalma sözleşmesinin koşulları, başlığa ve sözleşme tarafından etkilenen tüm sipariş satırlarına kopyalanır.


## <a name="create-a-new-purchase-agreement"></a>Yeni bir satınalma sözleşmesi oluşturun.
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma sözleşmeleri > Satınalma sözleşmeleri** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Satıcı hesabı** alanında, açılan menüyü seçin ve istediğiniz kaydın satırını seçin.
4. **Satınalma sözleşmesi sınıflandırması** alanında, açılan menüyü seçin ve istediğiniz kaydın satırını seçin.
5. **Genel** hızlı sekmesini genişletin.
6. **Bitiş tarihi** alanına bir tarih girin.

    - Bu bitiş tarihi tüm taahhüt satırları için varsayılan olacaktır ve her bir taahhüdün ne kadar süreceğini belirleyecektir.  

7. **Belge başlığı** alanına satınalma sözleşmeniz için ad yazın.

    - **Varsayılan taahhüt** alanını **Ürün miktarı taahhüdü** olarak bırakın (veya bunun için ayarlanmamış ise buna çevirin).  
    - Varsayılan taahhüt değeri, sözleşme satırlarındaki seçeneklerinizi belirler. Sözleşme satırlarını oluştururken yeni bir taahhüt türüne ihtiyaç duyarsanız, başlıktaki varsayılan taahhütü değiştirmeniz gerekir. 4 tür taahhüt vardır. **Ürün miktarı taahhüdü**, belirli bir miktar ürün için. **Ürün değeri taahhüdü**, bir ürünün belirli bir para birimi tutarı için. **Ürün kategori değeri taahhüdü**: Bir tedarik kategorisindeki para birimi miktarı için, miktarın katalogda mevcut olan veya olmayan bir madde için. **Değer taahhüdü**, belirli bir para birimi miktarı için herhangi bir ürün veya herhangi bir tedarik kategorisi kullanılarak yerine getirilebilmek üzere.  

8. **Tamam**'ı seçin.

## <a name="add-a-commitment"></a>Taahhüt ekleyin
1. **Satır ekle**'yi seçin.
2. **Madde numarası** alanında, açılır menüden istediğiniz kaydı seçin.
3. **Miktar** alanına bir sayı girin. Bu, satıcınızdan satın almak üzere anlaştığınız toplam miktarıdır.  
4. **Birim fiyatı** alanına bir sayı girin.
5. **Satır ayrıntıları** bölümünü genişletin.
6. **Maksimum uygulanır** seçeneğini **Evet** olarak ayarlayın. **Maksimum uygulanır** seçeneği, taahhüdün kullanımını sınırlar. Yalnızca satır için **Miktar** alanında belirttiğiniz miktar kadar satın alabilirsiniz.  

## <a name="add-header-conditions"></a>Başlık koşulları ekleyin
1. Eylem Bölmesinde, **Seçenekler**'i seçin.
2. **Görünümü değiştir**'i seçin.
3. **Başlık görünümü**'nü seçin.
4. **Koşullar** bölümünü genişletin.
5. **Ödeme yöntemi** alanında, açılır menüden istediğiniz kaydı seçin. Satıcı hesabının ödeme koşulları burada varsayılan olarak gösterilir.  
6. **Teslimat şekli** alanında, açılır menüden istediğiniz kaydı seçin.
7. **Teslimat koşulları** alanında, aramayı açmak için açılır menü düğmesini seçin.

## <a name="confirm-and-activate-the-agreement"></a>Sözleşmeyi onaylayın ve etkinleştirin
1. Eylem Bölmesinde, **Satınalma sözleşmesi**'ni seçin.
2. **Onay**'ı seçin. **Anlaşmayı etkin olarak işaretle** seçeneğini **Evet** olarak ayarlayın.  
3. **Tamam**'ı seçin.
4. Eylem Bölmesinde, **Satınalma sözleşmesi**'ni seçin.
5. **Satınalma sözleşmesi onayları**'nı seçin. **Önizleme/yazdırma** seçeneği, bir belge yazdırmak veya satıcıya göndermek için bir satınalma anlaşması oluşturmanıza olanak sağlar. Daha sonra anlaşmayı günceller veya yeniden onaylarsanız, her iki sürüm de burada gösterilir.  
6. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]