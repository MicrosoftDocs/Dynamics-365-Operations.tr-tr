---
title: "Alacak ve Tahsilatları ayarlamak"
description: "Bu makale koleksiyonlar işlevselliği ayarlamayı açıklar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1982e495f740d6061b9574aa9f40f38180e8d110
ms.openlocfilehash: 76937aacbc1925603766299168ec2d4090bd161b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/03/2017

---

# <a name="set-up-credit-and-collections"></a>Alacak ve Tahsilatları ayarlamak

[!include[banner](../includes/banner.md)]


Bu makale koleksiyonlar işlevselliği ayarlamayı açıklar.

<a name="set-up-aging-period-definitions"></a>Yaşlandırma dönem tanımlarını ayarla
-------------------------------

Bir yaşlandırma dönemi tanımı ayarlayın. Bir yaşlandırma dönem tanımı **Yaşlandırma bakiyeleri**, **Tahsilat faaliyetleri**, ve **Tahsilat vakaları** liste sayfaları üzerinde görüntülenen sütunları tanımlar. Bu ayrıca, **Tahsilatlar** sayfasında görüntülenen periyotları da tanımlar. Bir müşteri havuzu ayarlanmışsa, havuzun eskime dönem tanımı kullanılır. Hiçbir havuz ayarlanmamışsa, **Alacak hesapları parametreleri** sayfasındaki varsayılan eskime dönem tanımı kullanılır. Hiçbir varsayılan yaşlandırma dönemi tanımı belirtilmemişse, **Yaşlandırma dönemi tanımları** sayfasındaki ilk yaşlandırma dönemi tanımı kullanılır.

## <a name="create-an-aging-snapshot"></a>Bir Yaşlandırma anlık görüntüsü oluştur
Tüm müşteriler veya bir müşteri havuzundaki müşteriler için yaşlandırma anlık görüntüsü oluşturun. Yaşlandırma anlık görüntüsü bilgisi,**Yaşlandırılmış bakiyeler** listesi sayfası ve **Tahsilatlar** sayfasında görüntülenir. Liste sayfasını kullanmadan önce bir yaşlandırma anlık görüntüsünü oluşturmanız gerekir. Liste sayfası sadece yaşlandırma anlık görüntüsü oluşturulan müşterilerin bilgilerini gösterir.

## <a name="optional-set-up-customer-pools"></a>İsteğe bağlı: Müşteri havuzlarını ayarla
Müşteri havuzlarını, müşteri gruplarını temsil etmek üzere ayarlayabilirsiniz. Müşteri havuzlarını, **Tahsilatlar** listesi sayfalarında, **Tahsilatlar** sayfasında veya yaşlandırma anlık görüntüsü oluşturduğunuzda, müşteri bilgisini filtrelemek üzere kullanabilirsiniz.

## <a name="optional-create-a-collections-team"></a>İsteğe bağlı: Tahsilatlar takımı oluşturma
Kuruluşunuzda birden çok kişi tahsilatlarla uğraşıyorsa, bir tahsilatlar ekibi ayarlayabilirsiniz. Takımı **Alacak hesapları parametreleri** sayfasında seçebilirsiniz. Eğer bir tahsilat takımı oluşturmazsanız, **Tahsilatlar aracısı** sayfasında tahsilat acentaları oluşturduğunuzda bir takım otomatik olarak oluşturulacaktır.

## <a name="set-up-a-collections-case-category"></a>Tahsilat vakaları kategorisi ayarlayın
Koleksiyonları çalışmanızı organize etmek için vakalar kullanacaksanız, **Tahsilatlar** kategori türünde olan bir vaka kategorisi ayarlayın. Bu kurulum yalnızca **Tahsilatlar** sayfası üzerinde vaka işlevini kullanmak istiyorsanız gereklidir.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Günlük adlarını ayarlama (kapatma, silme ve NSF)
Hareketleri **Tahsilatlar** sayfası üzerinde işlendiğinde kullanılan günlük adları ayarlama. Bu işlem bir hareketin kapatılması, bir hareketin silinmesi ve yetersiz fon (NSF) ödeme işlenmesini kapatılmasını içerir.

| Açıklama | Günlük türü:     |
|-------------|------------------|
| Kapatma  | Müşteri ödemesi |
| Sil   | Günlük            |
| Karşılıksız         | Müşteri ödemesi |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Silme hareketleri için bir neden kodu ayarlama
**Tahsilatlar** sayfasında hareketler silindiğinde varsayılan olarak kullanılacak sebep kodunu ayarlamak. Silme işlemi süresinde kodu değiştirebilirsiniz.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>E-posta ekleri için bir klasör ayarlayın ve e-posta şablonları oluşturun
**Tahsilatlar** sayfasından, Microsoft Excel eklerine sahip e-postalar gönderirseniz, bu iletiler için isteğe bağlı e-posta şablonları oluşturabilirsiniz.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Tahsilatlar için alacak hesapları parametreleri ayarla
**Tahsilatlar** sekmesinde görüntülenen alacak hesapları parametrelerini ayarlamak.

## <a name="optional-set-up-collections-agents"></a>İsteğe bağlı: Tahsilat temsilcilerini ayarla
Kuruluşunuzda birden çok kişi tahsilatlarla uğraşıyorsa, bir tahsilat temsilcileri ayarlayabilirsiniz. Tahsilat temsilcisi, **Kullanıcı ilişkileri** sayfasında bir kullanıcı olarak ayarlanmış bir çalışandır. Aracıların işlerini düzenlemelerine yardım etmek için, tahsilat aracılarına müşteri havuzları (müşteri sorguları) atayabilirsiniz. Tahsilat temsilcileri, **Alacak hesapları parametreleri** sayfasında seçilen takıma eklenir. Sayfa üzerinde bir takım seçili değilse, **Tahsilatlar** adlı yeni bir takım otomatik olarak oluşturulur ve Tahsilat temsilcileri bu takıma eklenir.

## <a name="set-up-a-writeoff-account"></a>Silme hesabı ayarlama
Genel muhasebe defterinde bir hareket silineceği zaman, silme girişinde kullanılacak bir silme hesabı ayarlayın. Bu hesap, müşteri deftere nakil profili üzerinde depolanır.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Banka hesapları için NSF bilgisi ayarlayın
NSF ödemeleri **Tahsilatlar** sayfasında tanımlandığında doğru günlüğe sahip olmaları için banka hesaplarını güncelleştirin. **Para birimi yönetimi** sekmesinde, **NSF ödeme günlüğü** alanında, bir ödeme günlüğünü seçin.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Tahsilatlar sayfasının kullanıcıları için Outlook ayarları belirleyin
Çalışanlar faaliyetler yaratabilmeden veya **Tahsilatlar** sayfasını kullanarak e-posta iletileri gönderebilmeden önce, **Microsoft Outlook eşitlemesi** yapılandırma anahtarının seçili olduğunu ve bu çalışanlar için Outlook eşitlemesinin ayarlanmış olduğunu doğrulamak zorundasınız.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Tahsilat müşteri ilgili kişileri için e-posta ve adres ayarları ayarlama
Bu kişilere **Tahsilatlar** sayfasından e-posta iletileri göndermek istiyorsanız, müşteri ilgili kişi için e-posta adreslerini ayarlayın. Tahsilatlar ilgili kişisi, **Tahsilatlar** sayfasında varsayılan ilgili kişisi olarak kullanılır. Eğer bir müşteri için ekstrelerde birincil adresinden farklı bir adres kullanılacaksa, bunun için bir ekstre adresi ayarlayabilirsiniz. 

Bir müşterinin **Kredi ve Tahsilatlar** hızlı sekmesinde, **Tahsilatlar kişisi** alanında, müşteri kuruluşta sizin tahsilat temsilcinizle işbirliği yapan kişiyi seçin. Bu kişi **Tahsilatlar** sayfasında varsayılan kişi olarak kullanılır ve e-posta iletileri ona gönderilir. 

> [!NOTE] 
> Müşteri için, tahsilatlarla ilgili bir kişi belirtilmezse, müşteri için birincil ilgili kişi kullanılır. Eğer birincil bir ilgili kişi belirtilmemişse, e-posta iletileri **Kişiler** sayfasında ilk sırada listelenen kişiye gönderilir.

## <a name="set-up-email-settings-for-salespeople"></a>Satış elemanları için e-post ayarlarını ayarlamak
**Tahsilatlar** sayfasından satış elemanlarına e-posta iletileri göndermek istiyorsanız, satış elemanları için e-posta adreslerini ayarlayın. Her komisyon satış grubundaki her satış temsilcisi için bir e-posta adresi ayarlayın. **Kişi** seçeneği işaretli olan satış temsilcisi, e-posta iletilerinin gönderileceği varsayılan satış elemandır. 

Bir satış temsilcisi belirtilmezse, müşteri kuruluşun birincil satış temsilcisi kullanılır. Birincil satış temsilcisi belirtilmezse, e-post iletileri sayfada listelenen ilk satış elemanına gönderilir.


Daha fazla bilgi için aşağıdaki konulara bakın:

 - [Tahsilat mektubu sırası oluşturma](tasks/create-collection-letter-sequence.md)
 
 - [Tahsilat mektuplarını işleme](tasks/process-collection-letters.md)
 
 - [Tahsilat bilgilerini gözden geçirme](tasks/review-collections-information.md)


