---
title: Satın alma siparişi oluştururken satın alma sözleşmesini uygulama
description: Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.
author: Henrikan
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130524dc8e0c8724e35bf13c6b250ab721383711
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570381"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Satın alma siparişi oluştururken satın alma sözleşmesini uygulama

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir. Satın alma siparişi başlığına kopyalanacak genel terimler olduğundan, satınalma siparişi oluşturduğunuzda satın alma sözleşmesinin uygulanması gereklidir. Genellikle bu görev bir satınalma aracısı tarafından gerçekleştirilir. Bu kılavuz için bir önkoşul olarak bir satıcı ve öğeler için bir ürün miktarı taahüdüne sahip etkili satınalma anlaşmanızın olması gerekir. Aynı yordam, diğer tür taahhütleri içeren bir satın alma sözleşmeniz varsa da kullanılabilir.

## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Üretim ve kaynak \> Çalışma alanları \> Satın alma siparişi hazırlama**'ya gidin.
1. Eylem Bölmesinde **Yeni satınalma siparişi**'ni seçin.
1. **Satınalma siparişi oluştur** iletişim kutusu açılır. **Satıcı hesabı** seçin. Diğer adres alanlarını inceleyin ve gerektiği gibi ayarlayın.
1. **Genel** hızlı sekmesini genişletin.
1. **Satınalma anlaşması** alanında, kullanmak istediğiniz etkin anlaşmayı bulun ve seçin. Satıcı için kullanılabilir tüm sözleşmeler burada listelenir.  
1. **Evet**'i seçin.
1. **Tamam**'ı seçin.

## <a name="add-a-line"></a>Satır ekleyin

1. **Madde numarası** alanına bir değer girin. Taahhüt üzerinde belirli stok ve konum boyutları mevcutsa, sözleşmeden faydalanabilmeniz için satınalma siparişi satırında aynı değeri girmeniz gerekir.
1. **Site** alanında, aramayı açmak için açılır menü düğmesini seçin. Siparişte veya satıcıda varsayılan olarak bulunan değer halihazırda tesis için girilmiş olabilir. Bu durumda, bu adımı atlayın.  
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Miktar** alanına bir sayı girin. Fiyatın taahhütten kopyalandığını doğrulayın.  

## <a name="look-up-the-commitment"></a>Taahhüdü bulun

1. **Satırı güncelleştir**'i seçin.
1. **Eklendi**'yi seçin. Burada satın alma sözleşmesinin ayrıntılarını alabilirsiniz. Örneğin, fiyatı ve fiyatın ve iskontonun sabit olup olmadığını görebilirsiniz, bu da satınalma siparişi üzerindeki fiyatınızı ya da iskontonuzu taahhüdün üzerinde bulunandan değiştirirseniz, sistemin bağlantıyı kaldırarak satınalma siparişi satırının taahhüdü yerine getirmesinin önüne geçer. Ayrıca, taahhüdün üzerindeki miktarın, taahhüdü yerine getiren tüm siparişlerin toplamını geçemeyeceği anlamına gelen, Maksimum uygulanır kuralının seçili olup olmadığını da görürsünüz.  
1. Sayfayı kapatın.

## <a name="look-up-the-purchase-agreement"></a>Satınalma sözleşmesi'ni bulun

1. **Eylem Bölmesinde**, **Genel**'i seçin.
1. **Satınalma anlaşması**'nı seçin.
1. Sayfayı kapatın.
1. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]