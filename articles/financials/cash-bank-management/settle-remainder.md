---
title: "Kalanı kapat"
description: "Ayırma etkinliğinden kalan tutarı, bu tutarı bir genel muhasebe hesabına uygulayarak kapatabilirsiniz."
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: e67bd36adc92bffea48087d0322ab14e9c066a4e
ms.contentlocale: tr-tr
ms.lasthandoff: 12/06/2018

---

# <a name="settle-remainder"></a>Kalanı kapat

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

Ayırma etkinliğinden kalan tutarı, bu tutarı bir genel muhasebe hesabına veya başka bir müşteriye uygulayarak kapatabilirsiniz. Kalan tutarları bir günlüğe girdiğinizde veya yalnızca açık işlemleri kapattığınızda, kalan tutarı kapatabilirsiniz.

## <a name="setting-up-defaults"></a>Varsayılanlarını ayarlamak 
Kalanı kapatı kullanmadan önce Kalanı kapat özelliğini etkinleştirmeniz ve varsayılan ayarları belirlemeniz gerekir

1)  **Alacak hesapları > Parametreler > Kapatmalar** veya **Borç hesapları > Parametreler > Kapatmalar** üzerine tıklayın
2)  **Kapatma** sekmesini seçin ve **Kalanı kapatmayı ektinleştir** üzerine tıklayın
3)  **Varsayılan neden kodu**'nda, bir varsayılan neden kodu seçin. Bir neden konunun **Alacak hesapları > Kurulum > Müşteri silme neden kodları** veya **Borç hesapları > Kurulum > Müşteri silme neden kodları**'nda halihazırda ayarlanmış olması gerekir. **Varsayılan kalan kapatma hesabı**, silme neden kodunun atanmış olduğu hesaba varsayılan olacaktır.
3)  **Varsayılan kalan kapatma hesabı**'nı gerekli şekilde güncelleştirin.
4)  **Varsayılan günlük adı** içinde, yalnızca çık işlemleri kapatıyorsanız, bir ödeme günlüğü oluşturmak istediğinizde kullanılacak olan bir ödeme günlüğü seçin. Kalanı kapat özelliğini etkinleştirirseniz, bir varsayılan günlük adı eklemeniz gerekir.

## <a name="settle-remainder-from-a-journal"></a>Bir günlükten kalanı kapat
**Kalanı kapat** özelliğini etkinleştirmezseniz, yine de bir hareketi bir günlüğe girebilir ve geçmişte yapmış olduğunuz gibi hareketleri buna karşı kapatabilirsiniz. **Tamam** düğmesine tıkladığınızda, fatura üzerindeki açık bakiye, nakit tutar kadar azaltılır. Nakit, faturayı tümüyle kapatmıyorsa, fatura, daha sonra kapatılmak üzere bir kalan tutar ile açık kalır.

**Kalanı kapat** özelliği etkinleştirilmişse, kalan tutarı bir genel muhasebe hesabına kapatabilirsiniz. Ayrıca, faturaları açık bırakmak yerine kalanı başka bir müşteri hesabına aktarabilirsiniz (müşteri hareketleri için) veya başka bir satıcıya aktarabilirsiniz (satıcı hareketleri için). 

**Kapatma** sayfasından kalanı kapatmak için aşağıdaki adımları gerçekleştirin:

1)  **Kapatma** sayfasında, kapatmak istediğiniz faturaları veya hareketleri işaretleyin.
2)  **Kalanı kapat** düğmesine tıklayın.
3)  Bir genel muhasebe hesabına karşı kapatılacak tutarı, kalanı kapatmakta kullanılacak tarihi, parametrelerden varsayılan neden kodunu ve parametrelerden varsayılan hesabı gösteren bir iletişim kutusu görüntülenir. 
4)  Varsayılan nedeni değiştirmek isterseniz yeni bir kapatma nedenini seçin. Kapatma hesabı, neden kodunda ilişkilendirilmiş olan ilgili hesaba değiştirilecektir.
5)  Değiştirmek istiyorsanız, kapatma hesabını düzenleyin.
6)  Müşteri hareketlerini kapatıyorsanız ve kalanın başka bir müşteriye taşınmasını istiyorsanız, **Kalanı bir müşteri hesabına kapat**'ı seçin. Satıcı hareketlerini kapatıyorsanız ve kalanın başka bir satıcıya taşınmasını istiyorsanız, **Kalanı bir satıcı hesabına kapat**'ı seçin.
6)  **Kalanı kapat**'ı tıklatın.
7)  **Günlük** sayfası görüntülenir. Bir başka günlük satırı, kalanı kapat tutarı ile günlüğe tutar olarak ve kalanı kapat hesabı mahsup hesap olarak eklenir. Kapatma tutarını başka bir müşteri veya satıcıya taşımak için bir müşteri veya satıcı eklediyseniz ek bir satır günlüğe kapatma tutarını bu müşteri veya satıcıya taşımak için eklenir.

Günlüğü deftere naklederken, açık hareket tam olarak kapatılır. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Kalanı, yalnızca açık hareketleri kapatılırken kapatma
Bir günlük olmadan açık hareketleri kapattığınızda da kalanı kapatabilirsiniz.

Kalanı kapatmak için aşağıdaki adımları uygulayın:

1)  **Kapatma** sayfasında, kapatmak istediğiniz faturaları veya hareketleri işaretleyin
2)  **Kalanı kapat** üzerine tıklatın.
3)  Bir genel muhasebe hesabına karşı kapatılacak tutarı, kalanı kapatmakta kullanılacak tarihi, parametrelerden varsayılan neden kodunu ve parametrelerden varsayılan hesabı gösteren bir iletişim kutusu görüntülenir. 
4)  Varsayılan nedeni değiştirmek isterseniz yeni bir kapatma nedenini seçin. Kapatma hesabı, neden kodunda ilişkilendirilmiş olan ilgili hesaba değiştirilecektir.
5)  Değiştirmek istiyorsanız, **kapatma hesabını** düzenleyin.
6)  Müşteri hareketlerini kapatıyorsanız ve kalanın başka bir müşteriye taşınmasını istiyorsanız, **Kalanı bir müşteri hesabına kapat**'ı seçin. Satıcı hareketlerini kapatıyorsanız ve kalanın başka bir satıcıya taşınmasını istiyorsanız, **Kalanı bir satıcı hesabına kapat**'ı seçin.
7)  Kalan kapatma ile bir ödeme günlüğü oluşturmayı da seçebilir veya günlük olmadan da deftere nakledebilirsiniz. Bir ödeme günlüğü oluşturmak için **Günlük içinde düzenle** için **Evet**'i seçin. Oluşturduğunuz ödeme günlüğünü düzenleyebileceksiniz.
8)  **Kalanı kapat**'ı tıklatın. Bir günlük oluşturmak isterseniz, düğme **Günlük oluşturma** olarak değişecektir. Bunun yerine **Günlük oluştur**'u tıklatın.
9)  Bir ödeme günlüğü oluşturduysanız, günlük sayfası **Kalanı kapat**'ı tıkladıktan sonra açılır. Bir günlük satırı, kalanı kapat tutarı ile günlüğe tutar olarak ve kalanı kapat hesabı mahsup hesap olarak eklenir. Kapatma tutarını başka bir müşteri veya satıcıya taşımak için bir müşteri veya satıcı eklediyseniz ek bir satır günlüğe kapatma tutarını bu müşteri veya satıcıya taşımak için eklenir.

