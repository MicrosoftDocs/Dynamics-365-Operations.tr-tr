---
title: Satınalma sözleşmesinden satınalma sevk emri oluşturma
description: Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439239"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Satınalma sözleşmesinden satınalma sevk emri oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satınalma siparişi oluşturduğunuzda bir satın alma sözleşmesini kullanmayı gösterir. Satınalma siparişi başlığına kopyalanacak genel terimler olduğundan, satınalma siparişi oluşturduğunuzda satın alma sözleşmesinin uygulanması gereklidir. Genellikle bu görev bir satınalma aracısı tarafından gerçekleştirilir. Bu kılavuz için bir önkoşul olarak bir satıcı ve öğeler için bir ürün miktarı taahüdüne sahip etkili satınalma anlaşmanızın olması gerekir. Aynı yordam, diğer tür taahhütleri içeren bir satın alma sözleşmeniz varsa da kullanılabilir. Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz. USMF kullanıyorsanız, bu kılavuzu ayarlamak için gerekli önkoşulları sağlamak için "satın alma sözleşmesi oluştur" kılavuzunu çalıştırabilirsiniz.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. **Gezinti bölmesi**'nde, **Çalışma alanları > Satınalma siparişi hazırlığı**'ne gidin. 
2. **Yeni satınalma siparişi**'ne tıklayın.
3. **Satıcı hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Genel** hızlı sekmesini genişletin.
7. **Satınalma sözleşmesi** alanında, aramayı açmak için açılır menü düğmesine tıklayın. Satıcı için kullanılabilir tüm sözleşmeler burada listelenir. Kullanmak istediğiniz etkin sözleşmeyi bulun.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Evet** seçeneğini tıklatın.
10. **Tamam**'a tıklayın.

## <a name="add-a-line"></a>Bir satır ekleyin
1. **Madde numarası** alanına bir değer girin. Taahhüt üzerinde belirli stok ve konum boyutları mevcutsa, sözleşmeden faydalanabilmeniz için satınalma siparişi satırında aynı değeri girmeniz gerekir.  
2. **Site** alanında, aramayı açmak için aşağı açılır düğmeyi tıklayın. Siparişte veya satıcıda varsayılan olarak bulunan değer halihazırda tesis için girilmiş olabilir. Bu durumda, bu adımı atlayın.  
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Miktar** alanına bir sayı girin. Fiyatın taahhütten kopyalandığını doğrulayın.  

## <a name="look-up-the-commitment"></a>Taahhüdü bulun
1. **Satırı güncelleştir** öğesine tıklayın.
2. **İlişik** öğesine tıklayın. Burada satın alma sözleşmesinin ayrıntılarını alabilirsiniz. Örneğin, fiyatı ve fiyatın ve iskontonun sabit olup olmadığını görebilirsiniz, bu da satınalma siparişi üzerindeki fiyatınızı ya da iskontonuzu taahhüdün üzerinde bulunandan değiştirirseniz, sistemin bağlantıyı kaldırarak satınalma siparişi satırının taahhüdü yerine getirmesinin önüne geçer. Ayrıca, taahhüdün üzerindeki miktarın, taahhüdü yerine getiren tüm siparişlerin toplamını geçemeyeceği anlamına gelen, Maksimum uygulanır kuralının seçili olup olmadığını da görürsünüz.  
3. Sayfayı kapatın.

## <a name="look-up-the-purchase-agreement"></a>Satınalma sözleşmesi'ni bulun
1. **Eylem Bölmesi**'nde, **Genel** öğesine tıklayın.
2. **Satınalma sözleşmesi**'ne tıklayın.
3. Sayfayı kapatın.
4. Sayfayı kapatın.

