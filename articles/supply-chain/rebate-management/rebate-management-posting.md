---
title: İndirim yönetimi deftere nakil ayarı
description: Bu konuda, deftere nakil profilleri için veri ayarlama yöntemi açıklanmaktadır. Deftere nakil profilleri, indirim yönetimi hesaplama satırlarıyla ilgili deftere nakil girişlerini belirlemek için kullanılır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 808080d9e84c4af1b061d5a4ce76d5fa309e66f7
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216755"
---
# <a name="rebate-management-posting-setup"></a>İndirim yönetimi deftere nakil ayarı

[!include [banner](../includes/banner.md)]

İndirim yönetimi Deftere nakil profilleri, indirim yönetimi hesaplama satırlarıyla ilgili deftere nakil girişlerini belirlemek için kullanılır. Anlaşma başlığında bir deftere nakil profili seçildiğinde, bu tüm işlem satırları için geçerlidir.

Bu özellik şirketler arasında çalışır (tüzel kişilikler). Provizyonun tahakkuk ettirileceği ve talepleri ödeyecek şirketi belirtebilirsiniz. Ayrıca, kaynak deftere nakil şirketi başına farklı provizyon borç hesapları ve gider yazılacak alacak hesaplarını da ayarlayabilirsiniz.

Müşteriler ve satıcılar için indirim yönetimi deftere nakil profilleri ayarlamak üzere, **indirim Yönetimi \>i ndirim yönetimi deftere nakil kurulumu \> indirim yönetimi deftere nakil profilleri**'ne gidin. **İndirim yönetimi deftere nakil profilleri** sayfası, varolan tüm profillerinizi gösteren bir liste bölmesi içerir. Listeye profil eklemek veya bunları kaldırmak için eylem bölmesinde düğmeleri kullanabilirsiniz.

Bu konunun geri kalan bölümleri, bir profil oluşturduğunuzda veya düzenlediğinizde, kullanılabilir alanların nasıl kullanılacağını açıklar.

## <a name="posting-profile-header"></a>Profil başlığı nakletme

Aşağıdaki tabloda, her bir indirim yönetimi deftere nakil profilinin başlık bölümünde kullanılabilen ayarlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Deftere nakil profili | Profil için benzersiz bir ad girin. |
| Tanım | Profilin açıklamasını girin. |
| Modül | Profilin (*müşteri* veya *satıcı*) ilişkilendirildiği indirimlerin ve kâr paylarının türünü seçin. |
| Türü | Profil türünü seçin (*indirim* veya *kâr payı*). |
| Ödeme türü | <p>Bu alan, deftere nakledilen indirim çıktısının biçimini belirler.<p><p>**Tür** alanı *indirim* olarak ayarlandığında aşağıdaki değerler kullanılabilir:</p><ul><li>*Borç hesaplarını kullanarak öde*: Müşteri indirimini deftere naklettiğinizde, indirim müşterisinde ayarlanan havale satıcısının satıcı faturası oluşturulur. Satıcı indirimini deftere naklettiğinizde, indirim satıcısı hesabında satıcı faturası oluşturulur.</li><li>*Müşteri kesintileri*: İndirimi deftere naklederken, indirim müşterisi için bir müşteri kesintisi günlüğü oluşturulur.</li><li>*Vergi faturası Müşteri kesintileri*: İndirimi deftere naklederken, indirim müşterisi için bir serbest metin faturası oluşturulur.</li><li>*Ticari harcama*: İndirimi deftere naklederken, indirim müşterisi için bir müşteri kesintisi günlüğü oluşturulur.</li><li>*Raporlama*: İndirimi deftere naklederken, indirim müşterisi için bir müşteri kesintisi günlüğü oluşturulur.</li></ul><p>**Tür** alanı *Kâr payı* olarak ayarlandığında aşağıdaki değerler kullanılabilir:</p><ul><li>*Borç hesaplarını kullanarak öde*: İndirimi deftere naklettiğinizde, indirim satıcısı hesabında satıcı faturası oluşturulur.</li><li>*Raporlama*: İndirimi deftere naklettiğinizde, indirim satıcısı hesabında satıcı faturası oluşturulur.</li></ul><p>Daha fazla bilgi için, aşağıdaki [Ödeme türleri](#payment-types) bölümüne bakın. |
| Şirket | Provizyonun tahakkuk ettirileceği ve talepleri ödeyecek şirketi (tüzel kişilik) seçin. |

### <a name="payment-types"></a>Ödeme tipleri

Aşağıdaki tablo, **ödeme türü** alanının çeşitli ayarlarının, ödemelerin deftere nakledilme yerini nasıl etkilediğini özetler. Ödemeler, hedef işleme ve indirim türüne bağlı olarak bir müşteri hesabına, satıcı hesabına veya havale hesabına nakledilebilir.

| Ödeme türü | Hareket işlem türü | İndirim türü | Ödeme (fatura hesabı) |
|---|---|---|---|
| Borç Hesapları ile öde | Satıcı fatura günlüğü | Müşteri indirimi | Müşterinin havale satıcı hesabı |
| Borç Hesapları ile öde | Satıcı fatura günlüğü | Müşteri kâr payı | Satıcı hesabı |
| Borç Hesapları ile öde | Satıcı fatura günlüğü | Satıcı indirimi | Satıcı hesabı |
| Müşteri kesintileri | Günlük defter | Müşteri indirimi | Müşteri hesabı |
| Vergi faturası müşteri kesintileri | Dekont / Serbest metin faturası | Müşteri indirimi | Müşteri hesabı |
| Ticari harcama | Günlük defter | Müşteri indirimi | Müşteri hesabı |
| Raporlama | Günlük defter | Müşteri indirimi | Müşteri hesabı |
| Raporlama | Satıcı fatura günlüğü | Müşteri kâr payı | Satıcı hesabı |
| Raporlama | Satıcı fatura günlüğü | Satıcı indirimi | Satıcı hesabı |

> [!NOTE]
> [İndirim yönetimi anlaşmalarını](rebate-management-deals.md) ayarlarken aşağıdaki noktaları göz önünde bulundurun:
>
> - **Mutabakat ölçütü** alanının, *Anlaşma* olarak ayarlandığı anlaşmalar için deftere nakil sırasında dinamik anlaşma hesabını kullanamazsınız. Belirli bir müşteri veya satıcı hesabı kullanmalısınız.
> - **Mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için, müşteri her bir anlaşma satırı için ayarlandığından, anlaşma satırındaki dinamik bir anlaşma hesabına mahsup eden bir deftere nakil profili kullanabilirsiniz.

## <a name="posting-fasttab"></a>Deftere nakletme hızlı sekmesi

Aşağıdaki tabloda, her bir indirim yönetimi deftere nakil profilinin **Deftere nakletme** Hızlı sekmesinde kullanılabilen alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Alacak türü | Bir kayıt defteri hesabının mı, yoksa bir müşteri ya da satıcının mı alacaklandırılacağını seçin. |
| Alacak hesabı | İndirim provizyonları yapıldığında alacak tutarlarının deftere nakledildiği hesap. Bu hesap, indirim müşteriye alacak şekilde deftere nakledildiğinde borç hesabı olarak da kullanılır. |
| Günlüğün adı<br>(**Provizyon** bölümünde) | Deftere nakledilen provizyonu kaydetmek için kullanılacak günlüğün adını seçin. |
| Türü | İndirimin Bir kayıt defteri hesabına mı, yoksa bir müşteri ya da satıcıya mı nakledileceğini seçin. Başlıktaki **ödeme türü** alanı *vergi faturası müşteri kesintileri* olarak ayarlanmışsa, bu alan *müşteri/satıcı* olarak ayarlanır. |
| Hesap kaynağı kullanma | <p>Aşağıdaki değerlerden birini seçin:</p><ul><li>*Hiçbiri*: Bu değeri seçerseniz, indirim **hesabı alanında** bir hesap belirtmeniz gerekir.</li><li>*Anlaşma hesabı*: indirim satırında belirtilen müşteri veya satıcı hesabını kullanın. Bu değeri yalnızca **Mutabakat ölçütü** alanı, *Satır* ve **Hesap kodu** alanının anlaşma satırları *tablo* olarak ayarlandığı anlaşmalar için seçebilirsiniz. Müşteri kâr payı deftere nakil profilleri için geçerli değildir.</li></ul> |
| İndirim hesabı | Fiili indirim giderinin nakledileceği hesap. |
| Günlüğün adı<br>**(İndirim Yönetimi** bölümünde) | Müşteriye İndirim tutarı için alacak dekontunu naklederken kullanılacak günlüğün adını seçin. Başlıktaki **ödeme türü** alanı *vergi faturası müşteri kesintileri* olarak ayarlandığında bu alan kullanılamaz. |
| Madde satış vergisi grubu | İndirimin vergiye tabi olup olmayacağını belirtin. |
| Günlüğün adı<br>(**Gider yazma** bölümü) | Deftere nakledilen indirim provizyon ile aynı değilse, fark gider olarak yazılabilir. Deftere nakledilen gider olarak yazmayı kaydetmek için kullanılacak günlüğün adını seçin. |

## <a name="posting-by-company-fasttab"></a>Şirket bazında deftere nakil hızlı sekmesi

Her bir indirim yönetimi deftere nakil profilinin **şirket bazında deftere nakil** hızlı sekmesi, kılavuzda her şirket (yasal varlık) tarafından kullanılan deftere nakil hesabını belirtmenize olanak sağlar.

Kılavuza şirket eklemek ve bunları kaldırmak için araç çubuğundaki düğmeleri kullanın. Kılavuza her satır eklediğinizde, ilgili satır için yasal varlığı belirtmek üzere **Şirket** alanını kullanın. **Ad** alanı ardından otomatik olarak doldurulur.

Her bir şirket için bir satır seçin ve daha sonra kılavuzun altındaki alanları kullanarak aşağıdaki bilgileri girin:

- **Borç türü**: Bir kayıt defteri hesabının mı, yoksa bir müşteri ya da satıcının mı borçlandırılacağını seçin.
- **Borç hesabı**: İndirim provizyonları yapıldığında, borç tutarının nakledildiği hesabı girin.
- **Ana hesap**: Gider yazmalar için ana hesabı seçin.
