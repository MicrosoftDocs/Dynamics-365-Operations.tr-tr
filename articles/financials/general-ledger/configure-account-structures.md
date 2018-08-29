---
title: "Hesap yapıları yapılandır"
description: "Bu konu, hesap yapıları ve mali boyutlar hakkında bilgi sağlamaktadır."
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="configure-account-structures"></a>Hesap yapıları yapılandır

[!include[banner](../includes/banner.md)]

Hesap yapıları, siparişi ve hesap numarası girilirken kullanılan değerleri belirleyen bir kural dizisi oluşturmak için ana hesabı ve mali boyutları kullanır. İşiniz için gerektiği kadar hesap yapısı ayarlayabilirsiniz. Hesap yapıları, şirketin genel muhasebe kurulumuna atandığı için, paylaşılabilir.

Bir hesap yapısı oluştururken maksimum segment sayısı 11'dir. Bundan daha fazla segmente gereksiniminiz varsa, kurulumunuzu ve gereksinimlerinizi iyice değerlendirin çünkü bu, kullanıcı deneyimini etkileyecektir. Bir raporlama senaryosunda veri girişi yerine bir hiyerarşi veya kullanıcı tanımlı bir alan kullanarak segment türetilip türetilemeyeceğini değerlendirin. Örneğin konum üzerine rapor çıkarmak istiyorsanız ancak konumu departmanla ya da maliyet merkeziyle ifade edebiliyorsanız, konuma bir mali boyut olarak gereksiniminiz olmayacaktır. Değerlendirmenin ardından 11'den fazla segment gerektiği sonucuna varırsanız, gelişmiş kuralları kullanarak fazladan segment ekleyebilirsiniz.

Hesap yapıları için ana hesap gerekir. Ana hesabın yapıdaki ilk segment olması gerekmez ancak hesap numarası girişi sırasında hangi hesap yapısının kullanılmakta olduğunu belirler. Bu nedenle, bir ana hesap değeri ancak genel muhasebeye atanmış tek bir yapıda bulunabilir ve bu sayede değerler çakışmaz. Hesap yapısı belirlendikten sonra, olası yanlış günlük girişlerini azaltmak amacıyla, yalnızca geçerli boyut değerleri seçmesi için kullanıcıya yol göstermek üzere, izin verilen değerler listesi filtrelenir.

> [!NOTE] 
> Bütçelemeyi bir mali boyuta göre yapmayı düşünüyorsanız, mali boyut bir hesap yapısının parçası olmalıdır. Bütçelemede şu anda gelişmiş kurallar kullanılmıyor.

## <a name="example"></a>Örnek
Bir hesap yapısı ayarlamada en iyi yöntemi göstermek için bir şirketin bilanço hesaplarını (100000..399999) hesap ve iş birimi mali boyutu düzeyinde izlemek istediğini varsayalım. Gelir ve gider hesapları (400000..999999) için, şirket İş Birimi, Departman ve Maliyet Merkezi mali boyutlarını izliyor. Şirket bir satış yaptığı zaman Müşteriyi de izlemek istiyor. Bu senaryoyu kullanarak, şirketin genel muhasebesine atanmış iki hesap bulunması önerilir (biri Bilanço hesapları, diğeri Kar-Zarar hesapları için). Kullanıcı deneyimini ve doğrulamayı en iyi duruma getirmek için, Müşteri, ancak bir satış hesabı kullanıldığında kullanılan gelişmiş bir kural olmalıdır.

**Bilanço hesabı yapısı**

|Ana hesap          | İş birimi    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Kar-zarar hesabı yapısı**

|Ana hesap          | İş birimi    |Departman          | Maliyet merkezi    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Müşteri ekleme gelişmiş kuralı**

Ölçüt: Ana hesap 400000 ile 499999 arasındaysa müşteri ekleyin. Boş bırakılamaz.

|Müşteri         |
|-----------------|
|* |

Bu basitleştirilmiş örnekte tüm değerlere ve boş bırakmaya izin verildiği için * ve " " kullanılmaktadır.

## <a name="segments-and-allowed-values"></a>Segmentler ve izin verilen değerler
**Segmentler** ve **İzin verilen değer ayrıntıları** bölümünde, nakil sırasındaki doğrulamada izlenecek kuralları girmek için kılavuz tarzı bir deneyim sunulmaktadır. Kılavuzdaki hücrelere doğrudan yazabilir, Excel'den içe aktarabilir veya rehber olarak **İzin verilen değer ayrıntıları** bölümünden yararlanabilirsiniz.

**İzin verilen değer ayrıntıları** bölümü, **İşleçler** ("ile başlar", "arasında", "içerir" gibi birçok işleç) ölçüt oluştururken size yol gösterir.

[![İzin verilen değerler](./media/account.png)](./media/account.png) 

## <a name="more-than-7-criteria-needed"></a>7'den fazla ölçüt gerekli

7'den fazla ölçüte gereksiniminiz varsa, sonraki satırda ölçüt eklemeye devam edebilirsiniz. **İzin verilen değer ayrıntıları** bölümünde çalışırken, yedinci ölçütü girdikten sonra **+Yeni ölçütler ekle** işlevinin artık etkin olmadığı dikkatinizi çekecektir. Bu birçok etkene bağlıdır. Örneğin: 
 - Sütun genişliği 
 - Verilerin nasıl depolandığı 
 - **İzin verilen değer ayrıntıları** denetiminin performansı
 - Kullanılabilirlik  
 
Ölçüt eklemeye devam etmek için **Segmentte çoğalt** ve **İzin verilen değerler bölümüne** tıklayın. Bu, ölçütleri yeni bir satıra kopyalar. Daha sonra **İzin verilen değer ayrıntıları** bölümünde yazabilir veya değişiklik yapabilirsiniz.

(LINK TO VIDEO THAT WILL BE CREATED)

## <a name="best-practices"></a>Önerilen yöntemler
Hesap yapılarınızı ayarlarken takip edebileceğiniz bazı iyi uygulama örnekleri vardır. Ancak, iş bu yalnızca bir kılavuz niteliği taşımakta olup, işletmeniz, büyüme planınız ve bakım planınız hakkındaki bütünsel bir tartışma, o tartışmanın bir parçası olarak değerlendirilmelidir.

- Hesap girişi sırasında kullanıcıların en iyi destek sağlanan deneyimi elde etmeleri için, ana hesabı ilk sıraya getirin veya hesap yapısında mümkün olduğunca en öne yerleştirin.

- Tüzel kişiliklerinizde bakım yükünü azaltmak için hesap yapılarının mümkün olduğu kadar yeniden kullanın.

- Tüzel kişilikler arasındaki farklara yönelik olarak, hesap yapılarını yeniden kullanabilmek için gelişmiş kuralları kullanmayı düşünün.

- İzin verilen değerleri tanımlarken mümkün olduğunca aralıklar ve joker karakterler kullanın. Bu yalnızca bakım yükü olmadan büyümenize ve değişmenize olanak sağlamakla kalmaz, sistem de bu yapılandırma sayesinde daha ideal bir şekilde işler.

- Hesap yapısında her segment için yıldız işareti koymakla yetinmeyin, özel olarak gelişmiş kurallardan da yararlanın. Bu yönetimi zorlaştırabilir ve bakım sırasında sık sık kullanıcı hatasına neden olarak sistemde deftere nakil işlemini durdurabilir.

## <a name="account-structure-activation"></a>Hesap yapısı etkinleştirme
Yeni kurulumu veya bir hesap yapısında değişikliği yeterli bulduğunuz zaman yapıyı etkinleştirmeniz gerekir. Bir hesap yapısı genel muhasebeye atanırsa, bu etkinleştirme uzun süren bir işlem haline gelebilir çünkü sistemdeki deftere nakledilmemiş tüm hareketlerin yeni yapıya eşitlenmesi gerekir. Deftere nakledilmiş hareketler hesap yapısı değişikliklerinden etkilenmez.

Daha fazla bilgi için bkz. [Hesap planınızı hesaplama](plan-chart-of-accounts.md), [Mali boyutlar](financial-dimensions.md) ve [Hesap ve boyut kombinasyonları (segmentlere ayrılmış giriş kontrolü) girme](enter-account-dimension-combinations-segmented-entry-control.md).

