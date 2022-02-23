---
title: USMCA kaynak sertifikası
description: Bu özellik, ABD-Meksika-Kanada Anlaşması (USMCA) tarafından gerekli olan kaynak belgelerinin sertifikasını yazdırmanızı sağlar.
author: Henrikan
manager: tfehr
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 2263b3643becedd68911e2325c60ed4d97d6e823
ms.sourcegitcommit: ffb5998e611b83c2e4f98323f39e3e8f6419c652
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/02/2020
ms.locfileid: "4439770"
---
# <a name="usmca-certification-of-origin"></a>USMCA kaynak sertifikası

[!include [banner](../includes/banner.md)]

Bu özellik, ABD-Meksika-Kanada Anlaşması (USMCA) tarafından gerekli olan kaynak belgelerinin sertifikasını yazdırmanızı sağlar.

*USMCA kaynak belge sertifikası*, bildirim için gereken minimum veri öğelerini içerir. Bazı veri öğeleri yazdırmadan önce doldurulabilirken, diğerleri yazdırmadan sonra el ile doldurulmalıdır. Tercihi tarife işleminin yapılabilmesi için belgenin doldurulması ve beyannamenin verildiği tarihte ithalatçının elinde olması gerekmektedir. Belge ithalatçı, ihracatçı veya üretici tarafından doldurulabilir.

Belgeyi tek bir sevkiyat için **Tüm sevkiyatlar** listesi sayfasından veya **Sevkiyat ayrıntıları** sayfasından yazdırabilirsiniz.

Belgeye yalnızca tüzel kişiliğin birincil adresindeki ülke/bölge ABD olduğunda erişilebilir.

Belge yazdırma seçimine bağlı olarak belge, sisteminizden gelen verilerle önceden doldurulabilir. Yazdırılan belgeyi Microsoft Word gibi bir düzenleme biçimine dışarı aktararak yazdırılan belgeye veri değiştirmek veya eklemek mümkündür. Dışarı aktarmadan sonra, bir beyan yapmadan önce gerekli değişiklikleri uygulayabilirsiniz.

## <a name="turn-on-the-usmca-feature"></a>USMCA özelliğini etkinleştirme

USMCA özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Taşıma yönetimi*
- **Özellik adı:** *USMCA kaynak sertifikasyonu belgesi*

## <a name="document-content"></a>Belge içeriği

USMCA kaynak belgesi sertifikası aşağıdaki veri öğelerini içerir:

- Adres öğeleri
- Tasdik eden tarafın rolü
- Tekli sevkiyat
- Faturalar
- Paket dönem
- Madde ayrıntıları
- Sertifika verenin imzası
- Sayfa sayısı

Bu öğelerin her biri ve değerlerinin nasıl bulunduğu hakkında daha fazla bilgi için bu konunun kalan bölümlerine bakın.

## <a name="print-a-usmca-certification-of-origin-document"></a>USMCA kaynak sertifikasyonu belgesi yazdırma

Bir sevkiyatın USMCA kaynak belgesi sertifikasını yazdırmak için aşağıdakileri yapın:

1. Aşağıdakilerden birini yapın:
    - **Taşıma yönetimi > Sevkiyatlar > Tüm sevkiyatlar**'a gidin ve belgesini yazdırmak istediğiniz sevkiyatı seçin.
    - Belgesini yazdırmak istediğiniz sevkiyat için **Sevkiyat ayrıntıları** sayfasını açın (**Tüm sevkiyatlar** sayfasından dahil olmak üzere buraya gelmenin çeşitli yolları vardır).
1. Eylem Bölmesinde, **Sevkiyatlar** sekmesini açın ve **Yazdır** grubundan **USMCA kaynak sertifikası**'nı seçin.
1. **Kaynak sertifikası** iletişim kutusu açılır. Aşağıdaki alt bölümlerde açıklanan ayarları yapın ve belgeyi oluşturmak için **Tamam**'ı seçin.
1. Belgenin önizlemesi açılır. Belgeyi gerektiği gibi yazdırmak veya dışarı aktarmak için Eylem Bölmesi'nde sağlanan komutları kullanın.

### <a name="certifying-party"></a>Sertifikayı veren taraf

Belgeyi yazdıran taraf türünü belirlemek için **Sertifika veren taraf** açılır listesini kullanın. Sertifika veren tarafın *İhracatçı*, *İhracatçı ve Üretici*, *Üretici* veya *İthalatçı* olup olmadığını belirtin veya sertifikayı veren taraf bunlardan biri değilse boş bırakın. Seçtiğiniz seçenek, belgenin adres bölümlerinde nelerin yazdırılacağını belirler.

Seçtiğiniz **Sertifikayı veren taraf** yazdırılan belgeye eklenecektir.

Belge hem gelen hem de giden sevkiyatlar için yazdırılabilir. Yalnızca gelen sevkiyatlar için **Sertifikayı veren taraf** olarak *İthalatçı*'yı seçin.

Aşağıdaki tabloda, seçtiğiniz **Sertifikayı veren taraf**'a göre belgede yer alan bilgi türleri açıklanmaktadır.

| Sertifikayı&nbsp;veren taraf | Tanım |
|---|---|
| *\[Boş\]* | Belgeye aşağıdaki ayrıntıları ekler:<ul><li>**Sertifikayı verenin bilgileri**: Varsa sevkiyat ambarı için adres bilgilerini kullanır; aksi takdirde, varsa sevkiyat tesisi adresini kullanır; aksi takdirde Supply Chain Management'ta seçilen tüzel kişiliğin (şirket) adresini kullanır.</li><li>**İhracatçı bilgileri**: Boş</li><li>**Üretici bilgileri**: Boş</li><li>**İthalatçı bilgileri**: Boş</li><ul>|
| *İhracatçı* | Belgeye aşağıdaki ayrıntıları ekler:<ul><li>**Sertifikayı verenin bilgileri**: Varsa sevkiyat ambarı için adres bilgilerini kullanır; aksi takdirde, varsa sevkiyat tesisi adresini kullanır; aksi takdirde Supply Chain Management'ta seçilen tüzel kişiliğin (şirket) adresini kullanır.</li><li>**İhracatçı bilgileri**: Tüzel kişiliğin adres bilgilerini kullanır.</li><li>**Üretici bilgileri**: Boş</li><li>**İthalatçı bilgileri**: İlgili satış siparişinin fatura hesabını kullanır.</li><ul>|
| *İhracatçı ve Üretici* | Belgeye aşağıdaki ayrıntıları ekler:<ul><li>**Sertifikayı verenin bilgileri**: Varsa sevkiyat ambarı için adres bilgilerini kullanır; aksi takdirde, varsa sevkiyat tesisi adresini kullanır; aksi takdirde Supply Chain Management'ta seçilen tüzel kişiliğin (şirket) adresini kullanır.</li><li>**İhracatçı bilgileri**: Tüzel kişiliğin adres bilgilerini kullanır.</li><li>**Üretici bilgileri**: Tüzel kişiliğin adres bilgilerini kullanır.</li><li>**İthalatçı bilgileri**: İlgili satış siparişinin fatura hesabını kullanır.</li><ul>|
| *İthalatçı* | Belgeye aşağıdaki ayrıntıları ekler:<ul><li>**Sertifikayı verenin bilgileri**: Varsa sevkiyat ambarı için adres bilgilerini kullanır; aksi takdirde, varsa sevkiyat tesisi adresini kullanır; aksi takdirde Supply Chain Management'ta seçilen tüzel kişiliğin (şirket) adresini kullanır.</li><li>**İhracatçı bilgileri**: Boş</li><li>**Üretici bilgileri**: Boş</li><li>**İthalatçı bilgileri**: Tüzel kişiliğin adres bilgilerini kullanır.</li><ul>|
| *Üretici* | Belgeye aşağıdaki ayrıntıları ekler:<ul><li>**Sertifikayı verenin bilgileri**: Varsa sevkiyat ambarı için adres bilgilerini kullanır; aksi takdirde, varsa sevkiyat tesisi adresini kullanır; aksi takdirde Supply Chain Management'ta seçilen tüzel kişiliğin adresini kullanır.</li><li>**İhracatçı bilgileri**: Boş</li><li>**Üretici bilgileri**: Tüzel kişiliğin adres bilgilerini kullanır.</li><li>**İthalatçı bilgileri**: Boş</li><ul>|

### <a name="has-various-producers"></a>Çeşitli üreticileri var

**Sertifikayı veren taraf** açılır listesi, belgedeki üretici bilgileri için kullanılacak metni denetler. Aşağıdakilerden birini seçin:

- *Çeşitli üreticiler*: Üretici bilgilerine "Çeşitli" metnini yazdırır.
- *İstek üzerine sunulur*: Üretici bilgilerine "İthalat yetkililerinin talebi üzerine sunulur" metnini yazdırır.

**Sertifikayı veren taraf**, *İhracatçı ve Üretici* veya *Üretici* olarak ayarlandığında, **Çeşitli üreticileri var** ayarı geçersiz kılınır ve üreticinin adres bilgileri sertifikayı veren tarafınki ile aynı olur.

### <a name="blanket-period"></a>Paket dönem

Belge yalnızca bir sevkiyat için yazdırılmış olsa bile, belgenin aynı malların birden fazla sevkiyatını kapsayacağı bir paket dönemi oluşturmak için **Paket dönemi başlangıcı** ve **Paket dönemi bitişi** ayarlarını kullanın. Paket dönem tarihlerini herhangi bir kısıtlama olmaksızın ayarlayabilirsiniz ve belgeye eklenir. Ayrıca bu ayarları boş bırakabilir veya geçmişte ayarlayabilirsiniz.

### <a name="is-single-shipment"></a>Tekli sevkiyat

**Kaynak sertifikası** iletişim kutusunda, **Tek sevkiyat** ayarını aşağıdakilerden birine ayarlayın:

- *Evet*: "Tekli Sevkiyat: Evet" ifadesini fatura numarasının yanına ekler.
- *Hayır*: Hiçbir şey eklemez.

## <a name="other-information-included-in-the-document"></a>Belgede yer alan diğer bilgiler

**Kaynak sertifikası** iletişim kutusunu kullanarak seçtiğiniz isteğe bağlı öğelere ek olarak, USMCA kaynak sertifikası belgesi, aşağıdaki alt bölümlerde özetlenen bilgileri ve özel alanları içerir. Bu bilgilerden bazıları, belgeyi oluşturduktan sonra el ile girilmelidir.

### <a name="invoice-number"></a>Fatura numarası

Sevkiyatlarla ilgili satış faturalarının kodları, paket döneme bakılmaksızın belgeye yazdırılır. Fatura numaraları, **Tekli sevkiyat** seçimine bakılmaksızın yazdırılır.

### <a name="item-details"></a>Madde ayrıntıları

Belge, belirli madde ayrıntılarını listeleyen birkaç bölüm sağlar:

- **SKU numarası**: Serbest bırakılan ürünün madde numarasını yazdırır.

- **Açıklama**: Serbest bırakılan ürünün açıklamasını veya adını yazdırır. Kullanıcının dilinde açıklama varsa bu yazdırılır. Böyle bir açıklama yoksa, kullanıcının dilindeki ad yazdırılır. Bu ad yoksa, madde adı yazdırılır.

- **Uyumlaştırılmış Sistem (HS) Tarife Sınıflandırması**: Ürünle ilişkili Uyumlulaştırılmış Tarife Programı'nı yazdırır. Bu programları **Taşıma Yönetimi \> Kurulum \> Taşıma standardı \> Uyumlulaştırılmış Tarife Programları**'na giderek ayarlayabilirsiniz.

- **Kaynak ölçütü:** Belgeyi ilk kez yayınladığınızda bu bölüme verileri el ile girmeniz gerekir.

- **Menşe ülke:** Menşe ülkeyi yazdırır; bunu **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke**'ye (ayrıca bkz. [Menşe ülke](../pim/country-of-origin.md)) giderek uygulayabilirsiniz. Menşe ülkenin ISO kodu, sevkiyat teslim adresindeki hedefin ülkesine/bölgesine ve maddeye göre yazdırılır. Menşe ülke için herhangi bir veri ayarlanmazsa bu değer, **Serbest bırakılan ürün \> Dış ticaret \> Kaynak**'ta bulunan ayara geri alınır. Menşe ülke verileri hala bulunamıyorsa belgenin kaynak ülkesini el ile girmeniz gerekir.

### <a name="certifier-signature-and-date"></a>Sertifika verenin imzası ve tarih

Bunu, belgeyi oluşturduktan sonra el ile girmeniz gerekir.

### <a name="consists-of-number-of-pages"></a>Belgeyi oluşturan sayfa sayısı

Sertifikayı imzalayan kullanıcı, belgeyi oluşturduktan sonra sayfa sayısını el ile girmelidir (doğrulama için).

### <a name="page-numbers"></a>Sayfa numaraları

Belgenin alt kısmına yazdırılan geçerli sayfa ve sayfa sayısı.
