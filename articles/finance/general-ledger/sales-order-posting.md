---
title: Satış siparişi deftere nakli
description: Bu makale, stok deftere nakil profili sayfasının Satış siparişi sekmesi hakkında bilgi sağlar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886327"
---
# <a name="sales-order-posting"></a>Satış siparişi deftere nakli

**Stok deftere nakil profilleri** sayfasındaki **Satış siparişi** sekmesi satış siparişlerinin genel muhasebeye nasıl nakledileceğini denetlemek için kullanılır. Bir satış siparişi için genel muhasebeye iki ana faaliyet nakledilir: 

- Sevk irsaliyesi
- Fatura

Fiziksel bir hareketin (sevk irsaliyesi) bir satış siparişinin genel muhasebesine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:

- **Stok ve ambar yönetimi parametreleri** sayfasında, **Sevk irsaliyesini genel muhasebeye naklet** onay kutusunun işaretli olması gerekir.
- Satış siparişi satırındaki seçili madde için **Madde model grubu** sayfasında, **Genel muhasebedeki fiziksel stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
- **Stok deftere nakil profili** sayfasında, aşağıdaki deftere nakil türleri için ana hesaplar belirtilmelidir:
  - Birimlerin maliyeti, teslim edilen
  - Satılan malların maliyeti, teslim edilen

Mali bir hareketin (fatura) bir satış siparişinin genel muhasebesine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:

- Satış siparişi satırındaki seçili madde için **Madde model grubu** sayfasında, **Genel muhasebedeki mali stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
- Ana hesaplar **Stok deftere nakil profili** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
  - Birimlerin maliyeti, faturalanan
  - Satılan malların maliyeti, faturalanan
  - Gelir
  - İskonto\*

> [!NOTE]
> İskonto hesabı isteğe bağlıdır. GAAP ve IFRS gibi birçok muhasebe düzenlemeleri, iskontoların satış gelirini azaltmasını gerektirir ve bu nedenle bu hesaplar birçok senaryoda kullanılmaz. Yerel düzenlemeler izin veriyor ise, indirimli bir satış fiyatı bölümünü deftere nakletmek için ayrı bir ana hesap kullanın.

Bir satış siparişi için sevk irsaliyesi oluşturduğunuzda, ertelenen (tahmini) gelir değerini genel muhasebeye nakletmek için aşağıdaki koşulların karşılanması gerekir:

- Satış siparişi satırındaki seçili madde için **Madde model grubu** sayfasında, **Genel muhasebedeki fiziksel stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
- **Madde modeli grubu** sayfasında, **Satış Teslimatındaki Ertelenmiş Gelir Hesabına Naklet** onay kutusu seçilmelidir.
- **Stok ve ambar yönetimi parametreleri** sayfasında, **Sevk irsaliyesini genel muhasebeye naklet** onay kutusunun işaretli olması gerekir.
- **Stok ve ambar yönetimi parametreleri** sayfasında, **Fiziksel satış vergisini deftere naklet** onay kutusunun işaretli olması gerekir.
- **Alacak hesapları parametreleri** sayfasında, **Sevk irsaliyesini genel muhasebeye naklet** onay kutusunun işaretli olması gerekir.
- **Stok deftere nakil profili** sayfasında, aşağıdaki deftere nakil türleri için ana hesaplar belirtilmelidir:
  - Teslimatta ertelenmiş gelir
  - Teslimatta ertelenmiş gelir mahsubu
  - Teslimatta ertelenen satış vergisi

> [!NOTE]
> Genellikle, **Fiziksel stoğu deftere naklet** ve **Sevk irsaliyesini genel muhasebeye naklet** seçeneklerini etkinleştirmeniz önerilmektedir. Bu seçeneklerin etkinleştirilmesi ay sonu kapanış yordamlarını hızlandırmaya yardımcı olabilir, çünkü hiçbir ertelemenin el ile hesaplanması ve nakledilmesi gerekmeyecektir. Ek olarak, mali tablolar el ile müdahale olmadan ertelenen tutarları otomatik olarak yansıtır.

> [!IMPORTANT]
> **Satış Teslimatındaki Ertelenmiş Gelir Hesabına Naklet** seçeneği gelir kabulünde kullanılmaz. Gelir kabulü hakkında daha fazla bilgi için [Gelir tanımaya genel bakış](/accounts-receivable/revenue-recognition-overview.md) konusuna gidin

## <a name="sample-posting-profile-configuration"></a>Örnek deftere nakil profili yapılandırması 

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir:
 
- **Temizleme hesabı** sütunu, deftere nakil türünün bir temizleme hesabı olduğunu belirtir. Sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır. 
- **P/F** sütunu fiziksel deftere nakil için **P** ve mali deftere nakil için **F**'yi belirtir. 
- **İzle** sütunu belirli bir deftere nakil türü için ana hesabın genellikle başka bir deftere nakil türüyle aynı olup olmadığını gösterir. Sütundaki değer genellikle kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Bu ana hesaplar ve ana hesap adları yalnızca önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.


| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Birimlerin maliyeti, teslim edilen | 140100</br>140101 | Malzeme stoğu</br>Sevk edilip faturalanmayan malzemeler | Varlık | Kredi | Evet | P | Birimlerin maliyeti, faturalanan | Bir satış siparişi sevk irsaliyesi deftere nakledildiğinde kullanılır. Hesaba mahsup, satılan ve teslim edilen malların maliyetidir. Bir satış siparişi faturası deftere nakledildiğinde, bu hesaptaki tutar için ters işlem uygulanır. Fiziksel stoğu temsil etmek ve malzeme stoğu hesabını mali güncelleştirme için rezerve etmek amacıyla, sevk edilmiş ancak faturalanmamış malzemeler hesabını kullanmak isteyebilirsiniz. |
| Satılan malların maliyeti, teslim edilen | 500150 | Ertelenmiş SMM | Gider | Borç | Evet | P  | Bir satış siparişi sevk irsaliyesi deftere nakledildiğinde kullanılır. Hesaba mahsup, satılan ve teslim edilen birimlerin maliyetidir. Bir satış siparişi faturası deftere nakledildiğinde, bu hesaptaki tutar için ters işlem uygulanır. |
| Birimlerin maliyeti, faturalanan | 140100 | Malzeme stoğu | Varlık | Kredi | No. | C | Birimlerin maliyeti, teslim edilen | Bir satış siparişi faturası deftere nakledildiğinde kullanılır. Bu hesaba mahsup, satılan ve faturalanan malların maliyetidir. Bu hesap bilançonuzdaki stoğu temsil eder. |
| Satılan malların maliyeti, faturalanan | 500100 | SMM Malzemeleri | Gider | Borç | No. | C  | Bir satış siparişi faturası deftere nakledildiğinde kullanılır. Bu hesaba mahsup, satılan ve faturalanan birimlerin maliyetidir. Bu hesap, Kar/Zarar raporunuzda SMM'yi temsil eder. |
| Gelir (Satış siparişi geliri*) | 400100 | Gelir malzemeleri | Gelir | Kredi | No. | C   | Bir satış siparişi faturası deftere nakledildiğinde kullanılır. Bu hesaba mahsup, **Alacak hesapları deftere nakil profili**'ndeki Özet hesabıdır (Müşteri bakiyesi*). |
| Komisyon (Satış, komisyon*) | 602150 | Komisyon gideri | Gider | Borç | No. | C  | Komisyon etkinleştirildiğinde ve satış siparişi faturası işlemi sırasında deftere nakledildiğinde kullanılır. Bu hesaba mahsup, Komisyon borçlarıdır. |
| Komisyon mahsup (Satış, komisyon mahsup*) | 201110 | Komisyon borçları | Pasif | Kredi | Evet | C | Komisyon etkinleştirildiğinde ve satış siparişi faturası işlemi sırasında deftere nakledildiğinde kullanılır. Bu hesaba mahsup, Komisyon gideridir. |
| Teslimatta ertelenmiş gelir (Satışlar – sevk irsaliyesi geliri*) | 401400 | Tahakkuk eden satışlar | Gelir | Kredi | Evet | P  | Teslimatta ertelenmiş gelir etkinleştirildiğinde kullanılır ve bir satış siparişi sevk irsaliyesini işlediğinizde nakledilir. Bu hesaba mahsup, ertelenen gelir mahsubudur. Bu hesaptaki tutarlar için, satış siparişi faturasını deftere naklettiğinizde otomatik olarak ters işlem uygulanır. |
| Teslimatta ertelenmiş gelir mahsubu (Satışlar – sevk irsaliyesi gelir mahsubu)* | 130400 | Alacak hesapları – faturalanmamış | Varlık | Borç | Evet | P  | Teslimatta ertelenmiş gelir etkinleştirildiğinde kullanılır ve bir satış siparişi sevk irsaliyesini işlediğinizde nakledilir. Bu hesaba mahsup, teslimatta ertelenmiş gelirdir. Bu hesaptaki tutarlar için, satış siparişi faturasını deftere naklettiğinizde otomatik olarak ters işlem uygulanır. |
| Teslimatta ertelenen satış vergisi (Satışlar, sevk irsaliyesi vergisi*) | 250500 | Ertelenen satış vergisi | Pasif | Kredi | Evet | P  | Teslimatta ertelenmiş gelir etkinleştirildiğinde ve Fiziksel satış vergisini deftere naklet etkinleştirildiğinde kullanılır. Vergi tutarı, bir satış siparişi sevk irsaliyesini işlemek için deftere nakledilir. |

\*Bu tabloda parantez içinde gösterilen değerler, **Fiş hareketleri** sayfasındaki **Deftere nakil türü** alanında kullanılan değeri temsil eder. **Deftere nakil türü**'nü, **Fiş hareketleri** sayfasının **Genel** sekmesinde görüntüleyebilirsiniz.

## <a name="sales-category-posting"></a>Satış kategorisinin deftere nakli

Stok deftere naklini tüm maddeler, bir madde grubu veya tek bir madde için ayarlamaya alternatif olarak, kategorileri ayarlayabilir ve satış kategorilerine göre genel muhasebe deftere naklini denetleyebilirsiniz. Kategori hiyerarşisini ayarlama ve ürünlere kategori atama hakkında daha fazla bilgi için [Ürün sınıflandırması hiyerarşisi oluşturma](/supply-chain/pim/tasks/create-hierarchy-product-classification.md)ve [Kategori hiyerarşilerini kullanarak bir ürünü sınıflandırma](/supply-chain/pim/tasks/classify-product-category-hierarchies.md) konularına gidin.

Kategori hiyerarşisini oluşturduktan sonra, hiyerarşiyi bir veya daha fazla türe atamanız gerekir. Satış siparişlerinde kategori hiyerarşisi kullanmak için kategoriyi Satış kategori hiyerarşisi tipine atamanız gerekir. Daha fazla bilgi için [Kategori hiyerarşileri hakkında](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md) bölümüne gidin.

## <a name="create-revenue-posting-by-sales-category"></a>Satış kategorisine göre gelir deftere nakli oluşturma

Bir satış siparişine dayalı olarak bir satış siparişi için genel muhasebe nakil işlemleri atamak istiyorsanız, şu adımları izleyin:

1. **Stok yönetimi** > **Ayarlama** > **Deftere nakil** > **Deftere nakil**'e gidin.
2. **Satış** sekmesini seçin.
3. Yapılandırmak istediğiniz deftere nakil türü için radyo düğmesini seçin (örneğin **Gelir**).
4. **Yeni**'yi seçin.
5. **Madde kodu** alanında **Kategori**'yi seçin.
6. **Kategori ilişkisi** alanını kullanarak deftere nakil profili için kategoriyi seçin.
7. **Hesap kodu** alanında **Tablo**, **Grup** veya **Tümü** için bir seçenek belirleyin. Örneğin, deftere nakil profilini tüm müşterilere uygulamak için **Tümü** seçeneğini belirleyin.
   - 6. adımda **Tablo**'yu seçtiyseniz, **Hesap ilişkisi** alanında deftere nakil profili için belirli **Satıcı numarası**'nı seçin.
   - 6. adımda **Grup** öğesini seçtiyseniz, **Hesap ilişkisi** alanında deftere nakil profili için **Satıcı grubu**'nu seçin.
   - 6. adımda **Tümü** seçeneğini belirlediyseniz, **Hesap ilişkisi** alanı boş bırakılır.

8. Seçili nakil türündeki belirli bir vergi grubunu ilişkilendirmek üzere bir **Satış vergisi grubu** seçin. Bu alanı boş bırakırsanız, nakil tipleri tüm varolan vergi gruplarına uygulanır. Vergi grupları için belirtilen nakil yalnızca, satış ve satın almalar için yapılan hareketlere uygulanır.

9. **Ana hesap** alanında, hesap türünü deftere nakledeceğiniz hesap numarasını belirtin. Hesap planında varolan hesap numaralarından birini seçin.
