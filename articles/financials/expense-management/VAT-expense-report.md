---
title: "Gider yönetiminde KDV kurtarma"
description: "Bu konu uygun katma değer vergisi (KDV) hareketlerinde nasıl para iadesi alınacağını açıklar."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: tr-tr
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>Gider yönetiminde KDV kurtarma

[!include [banner](../includes/banner.md)]

Uygun katma değer vergisi (KDV) hareketlerinde para iadesi almak için bir şirket veya kuruluşun gerçek bilgileri tanımlaması, toplaması, doğrulaması ve göndermesi gerekir. Bu işlem birden çok görevi içerir ve şirketinizin boyutuna bağlı olarak bunlar çeşitli çalışanları veya rolleri içerebilir.

Gider yönetimi kullanarak KDV iadesi almak için aşağıdaki önkoşulların tamamlanmış olması gerekir:

- Gider kategorilerine tahsis edilen ülkeler/bölgeler için vergi kodlarının oluşturulması gerekir.
- Her vergi kodu için bir satış vergisi grubu oluşturulmalıdır.
- Her satış vergisi grubu için bir madde satış vergisi kodu oluşturulmalıdır.

Önkoşullar yerine getirildikten sonra çalışanlar KDV hareketleri için para iadesi istemek üzere aşağıdaki adımları izler.

1. Gider raporuna, uygun KDV iadelerini tanımlamak için kredi kartı hareketleriyle ilgili vergi bilgilerini girin.
2. Tüm vergi bilgilerin tam olduğunu doğrulayın ve sonra gider raporunu deftere nakledin.
3. Uluslararası KDV iadesi için uygun olan giderleri işleyin.
4. KDV düşme verilerini uluslararası vergiden düşme iadelerini dosyalayan üçüncü taraf satıcıya gönderin.
5. Yurtiçi KDV düşürme için giderleri işleyin.

Aşağıdaki bölümlerde Contoso çalışanlarının her adım nasıl tamamladığını gösteren örnekler verilmektedir.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Gider raporuna, uygun KDV iadelerini tanımlamak için kredi kartı hareketleriyle ilgili vergi bilgilerini girin

ABD'de yaşayan bir Contoso satış temsilcisi olan Nancy İngiltere'ye yaptığı bir iş seyahatinden döner. Seyahati sırasında yemekler için bazı kişisel kredi kartı harcamaları yapmıştır. Nancy'nin giderlerinin mutabakatını sağlamak için bir gider raporu oluşturması gerekir.

Nancy gider raporuna bilgileri girerken **Gider raporu Düzenle** sayfasındaki **Ülke/bölge** alanında **İngiltere**'yi seçer. Satış vergisi grupları listesi filtrelenir ve yalnızca İngiltere için geçerli olan gruplar gösterilir. Nancy **İngiltere 001** satış vergisi grubunu ve ardından **Yemekler** madde satış vergisi grubunu seçer. Daha sonra konaklama için yeni bir hareket ekler. İngiltere'de konaklama için yalnızca bir satış vergisi grubu ve madde satış vergisi grubu olduğundan, bu bilgi otomatik olarak Nancy'nin gider raporuna doldurulur.

Contoso ilkesi gereğince, tüm giderlerle eşleşen bir makbuz bulunması gerekir. Bu nedenle Nancy gider raporunu kaydeder, gider raporunda listelediği her hareket için bir makbuz eklemesi gerektiğini bildiren bir ileti alır. Nancy gider raporuna her harekete ait makbuzun dijital görüntüsünü eklediğini doğrular ve raporu onay için gönderir. Daha sonra, kağıt makbuzları arka ofis işlem ekibine gönderir. Bu ekip KDV iade verilerini, Contoso için uluslararası KDV iadeleri dosyalayan üçüncü taraf satıcıya gönderir.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Tüm vergi bilgilerinin eksiksiz olduğundan emin olun ve gider raporunu deftere nakledin

Contoso'da Borç hesapları koordinatörü olan April'ın rapor deftere nakledilmeden önce bir gider raporunda eksik olan vergi bilgilerini girmesi gerekir. **Gider raporu ayrıntıları** sayfasını açar ve Nancy'nin onaylanan gider raporunu görür. April hareketlerin ayrıntılarını görmek için gider raporunu açar. Nancy'nin hareketlerden biri için bir madde satış vergisi grubu girmediğini görür. Bu bilgi girilmediği için April gider raporunu deftere nakledemez. Bu nedenle, April Gider yönetiminin **Vergi yapılandırmaları** sayfasına bakar ve ülke/bölge ve hareket türü için uygun madde satış vergisi grubunu bulur. April artık gider raporunu genel muhasebeye nakledebilir.

April gider raporunu deftere naklettiğinde, KDV iade işi maddesi oluşturulur. Bu iş maddesi arka ofis işlem ekibinin bir üyesine atanır. April deftere nakil işleminin başarılı olduğunu belirten bir ileti alır. Bu ileti, iade için tanımlanmış olan KDV hareketi sayısını da listeler.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Uluslararası KDV iadesi için uygun olan giderleri işleme

Contoso arka ofis işlem ekibinin üyesi olan Arnie KDV iadesi için gerekli olan tüm bilgilerin gider raporlarına eklendiğini doğrulamaktan sorumludur. **Gider vergisi düşme** sayfasını açar ve Nancy'nin gönderdiği gider raporunu seçer. Arnie gerekli tüm makbuzların eklenmiş olduğunu ve doğru satış vergisi grubu ile madde satış vergisi kodlarının girilmiş olduğunu doğrular.

Arnie Nancy'den basılı kağıt makbuzları aldığında, kağıt makbuzlar ile dijital makbuzları karşılaştırır ve gider raporunun durumunu **Vergiden düşme için hazır** olarak değiştirir.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>KDV düşme verilerini uluslararası vergiden düşme iadelerini dosyalayan üçüncü taraf satıcıya gönderme

Arnie KDV düşürme iadelerini dosyalayacak olan üçüncü taraf satıcıya harcama raporu verilerini göndermeye hazır olduğunda **Gider vergisinden düşme** sayfasını açar. Sayfayı yalnızca **Vergiden düşme için hazır** olarak işaretlenmiş gider raporlarını gösterecek şekilde filtreler. Arnie daha sonra **Dosya** &gt; **Excel'e aktar**'ı seçer. Gider raporlarındaki KDV bilgileri Microsoft Excel çalışma sayfasına aktarılır. Tamer bu çalışma sayfasını üçüncü taraf satıcıya gönderir ve kağıt makbuzların postayla gönderilmiş olduğu iletisini ekler.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Yurtiçi KDV düşürme için giderleri işleme

Arnie'nin gider raporu hareketlerinin KDV düşürme için uygun olduğunu ve dijital makbuzların raporlara eklendiğini doğrulaması gerekir. Arnie yurtiçi veriden düşürme için uygun olan giderleri işlemeye başlamak için **Gider vergisinden düşme** sayfasını açar ve doğrulama gerektiren gider raporunu açar. Makbuzların çalışan yerine şirket adına olduğunu doğrular. KDV düşürülmesi için makbuzların şirket adına olması gerekir. Arnie sonra doğru satış vergisi grubu ve madde satış vergisi kodlarının uygulanmış olduğunu onaylar.

Arnie kağıt makbuzları aldığında, gider raporunun durumunu **Vergiden düşürme için hazır** olarak değiştirir. Daha sonra ilgili vergi dairesiyle iadeyi dosyalar. Bu durumda, ABD'deki uygun vergi dairesi Internal Revenue Service'tir (IRS).

