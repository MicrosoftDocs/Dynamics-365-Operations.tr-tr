---
title: Deftere nakil profillerine genel bakış
description: Bu makale, deftere nakil profillerinin Microsoft Dynamics 365 uygulamalarında nasıl kullanıldığını açıklamaktadır.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876138"
---
# <a name="posting-profiles-overview"></a>Deftere nakil profillerine genel bakış

Finans ve Operasyon uygulamalarında, yardımcı defter hesaplarının ana hesaplara nasıl dönüştürüldüğünü kontrol eden konfigürasyonları açıklamak için *deftere nakil profilleri* kullanılır; böylece, muhasebe defterine nakledilen hareketlerde kullanılabilirler. Örneğin, bir fatura deftere nakledildiğinde, müşterinin Alacak hesapları ana hesabına nasıl dönüştürüleceğini denetler.

Bazı modüller ve özellikler, adda "deftere nakil profili" sözcüklerini içeren bir sayfaya sahiptir (örneğin, **Müşteri deftere nakil profili** veya **Satıcı deftere nakil profili**). Ek olarak, bazı modüllerin, yardımcı defterden oluşturulan hareketler için deftere nakilleri konfigüre etme seçenekleri vardır. Örneğin, **Üretim denetim** modülünde deftere nakil işlemini üretim grubuna, kaynağa veya kaynak grubuna göre ayarlayabilirsiniz.

Birçok hareket türünde, profillerin deftere nakil için bir alternatif olduğunu unutmayın: deftere nakil tanımları. Desteklenen belgeler ile ilgili olarak, muhasebe girişlerindeki ana hesapları ve finansal boyutları sınıflandırmak için nakil profilleri yerine nakil tanımlarını kullanabilirsiniz. Zenginleşme veya ön yükümlülükler kullanmayı planlıyorsanız, hesap girişlerinin hesaplarını tanımlamak için bir deftere nakil tanımı gerekir.

Deftere nakil profilleri, deftere nakil tanımları veya **Otomatik hareketler sayfası hesaplarını** konfigüre etmeden önce, konfigüre etmek istediğiniz yasal varlıktaki **Genel muhasebe** sayfasında hesap planını konfigüre etmelisiniz.

## <a name="posting-types"></a>Deftere nakil türleri

Finans ve Operasyon uygulamalarında deftere nakil tipi bir borç veya alacak için genel kategori tanımlamak amacıyla kullanılır. Bu kategori, genel muhasebedeki ana hesaptan bağımsızdır. Genel muhasebede her borç veya alacak için deftere nakil türleri vardır.

Tek bir fişin bir veya daha fazla deftere nakil türü olabilir. Örneğin, hesap ve mahsup hesabın **Genel muhasebe** olarak ayarlandığı bir yevmiye defterinde deftere nakledilen bir hareket, hem borç, hem de alacak için **Genel muhasebe günlüğü** türünde olacaktır. Bunun tersine, satıcı faturası birden çok deftere nakil türüne sahip olacaktır. Bu deftere nakil türleri için, satıcı bakiyesi ve **Genel muhasebe günlüğü** gibi mahsup girişine ait ek satırlar için bir satır yer alır.

Deftere nakil türünü, **Fiş hareketleri** sayfasının **Genel** sekmesinde **Deftere nakil türü** alanında görüntüleyebilirsiniz.

> [!TIP]
> **Genel Bakış** sekmesindeki kılavuza **Deftere nakil** türü alanını eklemek veya taşımak için **Kişiselleştirme** araç çubuğunu kullanabilirsiniz. Bu şekilde, fişleri görüntülerken bu alanı daha kolay erişim veya görünüme getirebilirsiniz.

## <a name="detail-settings-for-a-posting-profile"></a>Deftere nakil profili için ayrıntı ayarları 

Deftere nakil profillerini konfigüre ettiğinizde, **Hesap kodu** alanı ayarın düzeyini tanımlar. Aşağıdaki seçenekler bulunur: **Tablo**, **Grup** ve **Tümü**. Eşleşme ilk eşleşmeden sonra durur ve sipariş en belirgin düzeyden en düşük düzeye doğru alınır. Bazı durumlarda **Hesap kodu** alanında biraz farklı bir ad olabilse de alanın davranışı ve işlevi aynı kalır. Örneğin, stok deftere nakil profili bir **Madde kodu** alanı ve bir **Hesap kodu** alanı içerir. Her iki alanda da **Tablo**, **Grup** ve **Tümü** değerleri bulunur.

**Ana hesap** alanı bir deftere nakil profili için boş bırakılmışsa ve **Otomatik hareket için hesaplar** sayfasında veya modüle özel veya özelliğe özgü bir sayfada ana hesap konfigüre etmediyseniz, deftere nakil türünü kullanan bir hareketi deftere naklettiğinizde hata iletisi alırsınız. İleti genellikle, "\[Deftere nakil türü hesabı\] bulunamıyor" olacaktır.

### <a name="table-value"></a>Tablo değeri

**Tablo** değeri, deftere nakil profiliyle ilişkilendirilmiş olan ana kayda işaret eder. Her tablo kaydı bir değere özgüdür. Bu değeri **Hesap kodu** alanından sonra görünen alanda belirtirsiniz. Genellikle bu alan **Hesap** veya **Hesap/Grup numarası** olarak adlandırılır. Tam ad, göründüğü sayfaya bağlı olarak değişir.

Örneğin, bir müşteri deftere nakil profiliyle çalışıyorsanız, **Tablo** değeri belirli bir müşteriyi temsil eder. Bu nedenle, **Hesap kodu** alanında **Tablo**'yu seçerseniz **Hesap/Grup numarası** alanında müşteri numarasını seçmeniz gerekir.

**Tablo** değeri en özel kayıt türünü gösterir. **Grup** veya **Tümü** değerinin seçildiği başka bir kayıt konfigüre edilmiş olsa bile, sistem her zaman bu değeri kullanır. Bu değer ayrıca, **Otomatik hareketler için hesaplar** sayfasında varsayılan değerler olarak oluşturduğunuz değerleri geçersiz kılar.

Her ana veri kaydı için ayrı bir deftere nakil profili tutuluyorsa, veri kalitesi sorunları oluşabileceğinden deftere nakil profillerinizi yönetmek için birincil mekanizma olarak **Tablo** değerini kullanmanız önerilmez. Ayrıca, her ana veri kaydı için ayrı bir deftere nakil profili bakımı ve mutabakat sağlaması da zordur. Bunun yerine, deftere nakil profillerinizin özel durumlarını yönetmek için bu değer kullanılmalıdır.

### <a name="group-value"></a>Grup değeri

**Grup** değeri, deftere nakil profiliyle ilişkilendirilmiş olan ana kayıt tarafından desteklenen gruplandırma kaydına başvurur. Her grup kaydı bir değere özgüdür. Bu değeri **Hesap kodu** alanından sonra görünen alanda belirtirsiniz. Genellikle bu alan **Hesap** veya **Hesap/Grup numarası** olarak adlandırılır. Tam ad, göründüğü sayfaya bağlı olarak değişir.

**Grup** değeri önce bir grubu konfigüre etmek ve bunu hesap için bir veya daha fazla kayda bağlamayı gerektiriyor. **Grup** değeri **Tablo** değerinden daha az, ancak **Tümü** değerinden daha belirgin. Bir tablo için kayıt konfigüre edilmemiş ise, sistem kaydın ait olduğu grup için bir kayıt bulmaya çalışır.

Örneğin, bir müşteri deftere nakil profiliyle çalışıyorsanız ve **Hesap kodu** alanında **Grup**'u seçerseniz , **Hesap/Grup numarası** alanında bir müşteri grubu seçmeniz gerekir. Müşteri grubunu **Müşteri grubu** sayfasında önceden tanımlamanız ve bir müşteri oluşturduğunuzda bir müşteri grubu belirtmeniz gerekir.

Belirli bir deftere nakil türü için birden çok ana hesabı izlemeniz gerekiyorsa, **Grup** değerini kullanmanızı öneririz. Örneğin, tahsil ettiğiniz üç Alacak hesabı ticaret ana hesabı vardır: normal müşteriler için bir adet, çalışanlar için bir adet ve şirketlerarası satış için bir adet. Bu durumda, müşterileri segmentlere ayırmak için üç müşteri grubu oluşturmanız önerilir. Sonra, her müşteri grubunu müşteri deftere nakil profilindeki doğru ana firmayla eşleyin. Aşağıdaki tabloda bu örnekteki üç müşteri grubu gösterilmektedir.

| Müşteri grubu | Ad | Açıklama |
|----------------|------|-------------|
| EXT | Harici müşteri | Bu grup tüm harici bağlantılı müşteriler için kullanılır. |
| EMP | Personel | Bu grup, kuruluşunuzdan satınalmalar yapan tüm çalışanlar için kullanılır. |
| INT | Şirketlerarası satışlar | Bu grup, tümleştirme satış ve satınalma siparişleriyle kullanılan tüm şirketlerarası müşteri hesapları için kullanılır. |

Deftere nakil profilinde üç satır ayarlarsınız. Her satırda, **Grup** değerini ve ilgili ana hesabı seçersiniz.

### <a name="all-value"></a>Tüm değer

**Tümü** değeri, ayarların tüm kayıtlar için geçerli olduğunu gösterir. **Hesap kodu** alanındaki **Tümü** değerini seçerseniz, **Hesap/Grup numarası** alanı kullanılamaz ve konfigürasyonu uygulamak için belirli bir kayıt seçemezsiniz.

**Tümü** değeri en az spesifik değerdir. Yalnızca, sistem **Tablo** veya **Grup** değeri için bir eşleşme bulamazsa kullanılır. Belirli bir deftere nakil türü için yalnızca bir ana hesabınız olduğunda, **Tümü** değerini seçmeniz gerekir.

Örneğin, bir müşteri deftere nakil profiliyle çalışırken, belirttiğiniz ana hesaplar, belirli bir tablo (müşteri) veya grup (müşteri grubu) için kayıt içermeyen tüm müşteriler ve müşteri grupları için geçerlidir.

### <a name="category"></a>Kategori

Stok deftere nakil profillerinde satış kategorisine veya tedarik kategorisine özgü ek bir değer bulunur. Bu değer **Tablo** değerine benzer ancak yalnızca belirli bir satış veya tedarik kategorisine uygulanır.

### <a name="default-value"></a>Varsayılan değer

**Hesap kodu** alanının **Tümü** olarak ayarlandığı bir deftere nakil profilinde deftere nakil türü için kayıt oluşturmazsanız ve sistem **Grup** veya **Tablo** değeri için eşleşen bir deftere nakil profili kaydı bulamazsa, sistem **Otomatik hareket için hesaplar** sayfasında belirtilebilen varsayılan değere geri döner. Daha fazla bilgi için bkz. [Otomatik hareketler için hesaplar](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Kliring hesapları

*Kliring hesabı* ifadesi muhasebede sık sık kullanılır. Microsoft Dynamics 365 uygulamalardaki bazı deftere nakil türleri kliring hesaplarıdır. Başka bir deyişle, başka bir hareket deftere nakledildiğinde, hesaptaki bakiye silinir veya ters kaydedilir. Örneğin, bir satınalma siparişi ürün girişini deftere naklettiğinizde, ürünlerin tahmini maliyetlerinin ve vergi ve satınalma siparişi satırlarındaki giderlerin toplamı, bir borç olarak satınalma tahakkuku deftere nakil türüne nakledilir. Daha sonra, satınalma siparişini faturaladığınızda bakiye, satınalma tahakkuku deftere nakil türünden tersine çevrilir ve Borç hesapları ticari hesabına taşınır.

## <a name="additional-resources"></a>Ek kaynaklar

Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Project Operations uygulamalarındaki birçok modül, deftere nakil profili veya genel muhasebeye nakil yöntemini denetleyen ek yapılandırmalara sahiptir. Her modüldeki deftere nakil profilleri ve deftere nakil kurulumları hakkında daha fazla bilgi edinmek için aşağıdaki konuları kullanın:

- [Otomatik hareketler için hesaplar](accounts-for-auto-transactions.md)
- [Borç hesapları deftere nakli](accts-payble-posting.md)
- [Alacak hesapları nakli](accts-recvble-posting.md)
- [Varlık kiralama nakli](../asset-leasing/set-up-lease-posting-accts.md)
- Kıymet yönetimi deftere nakli (Çok yakında)
- Nakit ve banka yönetimi (Çok yakında)
- Para birimi yeniden değerleme deftere nakil hesapları (Çok yakında)
- Gider yönetimi deftere nakli (Çok yakında)
- [Sabit kıymet deftere nakil profili](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Şirketlerarası muhasebe nakli (Çok yakında)
- Stok deftere nakil profili (Çok yakında)
- [Son teslim alma maliyeti deftere nakli](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Nakil tanımlarının genel bakışı](posting-definitions.md)
- Üretim denetim deftere nakli (Çok yakında)
- Proje yönetimi ve muhasebe nakli (Çok yakında)
- Hizmet yönetimi deftere nakli (Çok yakında)
- Vergi deftere nakli (Çok yakında)
- Zaman ve katılım deftere nakli (Çok yakında)
- Ulaşım yönetimi deftere nakli (Çok yakında)
- İndirim yönetimi deftere nakil profilleri (Çok yakında)
