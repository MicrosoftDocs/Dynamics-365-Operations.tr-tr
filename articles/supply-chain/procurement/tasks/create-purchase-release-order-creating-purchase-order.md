---
title: Satınalma siparişini oluştururken satınalma sevk emri oluşturma
description: Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.
author: kamaybac
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f02961f5f7da9bff389737b447e3b143dd72e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812287"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Satınalma siparişini oluştururken satınalma sevk emri oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir. Satınalma siparişi başlığına kopyalanacak genel terimler olduğundan, satınalma siparişi oluşturduğunuzda satın alma sözleşmesinin uygulanması gereklidir. Genellikle bu görev bir satınalma aracısı tarafından gerçekleştirilir. Bu kılavuz için bir önkoşul olarak bir satıcı ve öğeler için bir ürün miktarı taahüdüne sahip etkili satınalma anlaşmanızın olması gerekir. Aynı yordam, diğer tür taahhütleri içeren bir satın alma sözleşmeniz varsa da kullanılabilir. Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz. USMF kullanıyorsanız, bu kılavuzu ayarlamak için gerekli önkoşulları sağlamak için "satın alma sözleşmesi oluştur" kılavuzunu çalıştırabilirsiniz.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Satınalma siparişi hazırlama çalışma alanını açın.
2. Yeni satınalma siparişi'ne tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Genel bölümünün genişletilmiş görünümüne geçin.
7. Satınalma sözleşmesi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Satıcı için kullanılabilir tüm sözleşmeler burada listelenir. Kullanmak istediğiniz etkin sözleşmeyi bulun.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Evet'i tıklatın.
10. Tamam'a tıklayın.

## <a name="add-a-line"></a>Bir satır ekleyin
1. Madde numarası alanına bir değer girin.
    * Taahhüt üzerinde belirli stok ve konum boyutları mevcutsa, sözleşmeden faydalanabilmeniz için satınalma siparişi satırında aynı değeri girmeniz gerekir.  
2. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Siparişte veya satıcıda varsayılan olarak bulunan değer halihazırda tesis için girilmiş olabilir. Bu durumda, bu adımı atlayın.  
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Miktar alanına bir sayı girin.
    * Fiyatın taahhütten kopyalandığını doğrulayın.  

## <a name="look-up-the-commitment"></a>Taahhüdü bulun
1. Satırı güncelleştir öğesine tıklayın.
2. İlişik öğesine tıklayın.
    * Burada satın alma sözleşmesinin ayrıntılarını alabilirsiniz. Örneğin, fiyatı ve fiyatın ve iskontonun sabit olup olmadığını görebilirsiniz, bu da satınalma siparişi üzerindeki fiyatınızı ya da iskontonuzu taahhüdün üzerinde bulunandan değiştirirseniz, sistemin bağlantıyı kaldırarak satınalma siparişi satırının taahhüdü yerine getirmesinin önüne geçer. Ayrıca, taahhüdün üzerindeki miktarın, taahhüdü yerine getiren tüm siparişlerin toplamını geçemeyeceği anlamına gelen, Maksimum uygulanır kuralının seçili olup olmadığını da görürsünüz.  
3. Sayfayı kapatın.

## <a name="look-up-the-purchase-agreement"></a>Satınalma sözleşmesi'ni bulun
1. Eylem Bölmesinde, Genel öğesine tıklayın.
2. Satınalma sözleşmesi'ne tıklayın.
3. Sayfayı kapatın.
4. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]