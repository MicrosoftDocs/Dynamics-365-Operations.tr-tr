---
title: Diğer modüllerle bütçe planlama tümleştirmesi
description: Bütçe planları aşağıdaki çeşitli farklı kaynaklardan oluşturulabilir. Periyodik işlemin temel unsurları tüm kaynaklar için aynıdır.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d94e95c921d8237d8f69f793dbf48f1f40632964
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210349"
---
# <a name="budget-planning-integration-with-other-modules"></a>Diğer modüllerle bütçe planlama tümleştirmesi

[!include [banner](../includes/banner.md)]

 Bütçe planları aşağıdaki çeşitli farklı kaynaklardan oluşturulabilir. Periyodik işlemin temel unsurları tüm kaynaklar için aynıdır. 



<a name="periodic-processes-for-generating-budget-plans"></a>Bütçe planları oluşturmaya yönelik periyodik işlemler
----------------------------------------------

Bütçe planları aşağıdaki kaynaklardan oluşturulabilir:

-   Genel muhasebe hareketleri
-   Sabit kıymetler
-   Tahmin pozisyonları
-   Proje tahminleri
-   Tedarik tahminleri
-   Talep tahminleri
-   Bütçe kayıt girişleri
-   Diğer bütçe planları

Periyodik işlemin temel unsurları tüm işlemlerde aynıdır. Sekmeler, size verilerin kaynağını, hedef (bütçe planı) öznitelikleri ve işlemi bir toplu işlem olarak arka planda çalıştırmaya yönelik seçenekleri tanımlama olanağı sağlar. Bu makalenin sonraki bölümlerinde, her işlemde görüntülenmeyebilecek öğeleri tanımlayın.

### <a name="actions"></a>Eylemler

Her oluşturma işlemi için üç eylem uygulanabilir:

-   **Yeni bir bütçe planı oluşturmak** **Hedef** bölümünde seçilen özniteliklere sahip yeni bir plan oluşturur. Bu özniteliklerin benzersiz olması gerekmez. Bu nedenle, iki planın adları ve diğer değerleri aynı olabilir.
-   **Var olan bütçe planı senaryosunu değiştirmek** seçilen bütçe planı senaryosunda hedef bütçe planındaki tüm verileri siler ve seçilen kaynak verilerini kullanan yeni satırlar oluşturur.
-   **Var olan bütçe planı senaryosunu güncelleştirmek ve yeni veriler eklemek** hedef planda kaynak satırlarla eşleşen mevcut satırları günceller ve yeni veriler için yeni satırlar ekler. Eşleşme, genel muhasebe hesabına, tarihe, bütçe sınıfına ve diğer muhtelif alanlara dayanır. Örneğin, tahmin konumlarından bütçe planlarını oluştururken, konum numarası önemli bir alandır. Kaynak konum numarasıyla eşleşen bir konum numarası olan tüm satırlar, kaynaktan yeni satırlar ile değiştirilir.

### <a name="source"></a>Kaynak

Tüm işlemler için **Kaynak** sekmesi veriyi **Filtrele** düğmesini kullanarak filtrelemenizi sağlar. Varsayılan olarak, her işlem için filtreye belirli alanlar eklenir. Örneğin, **Genel muhasebeden bütçe planı oluştur** işleminde, **Genel muhasebe hesabı** ve **Ana hesap** kategorileri kullanılabilir ve oluşturma sayfasında görüntülenir. Filtreye eklediğiniz her alan, eklediğiniz her kriterle birlikte sayfaya da eklenir.

### <a name="target"></a>Hedef

**Hedef** öğesindeki **Geçmiş** seçeneği size bütçe planında yürürlük tarihi olarak kaynak verilerden tarihleri kullanma olanağı verir. Genellikle, yürürlük tarihi planın bütçe döngüsü içinde olmalıdır. **Geçmiş** seçeneğini **Evet** olarak ayarlarsanız, kaynağı tarihi (hatta yılı) kullanılır, böylece geçmiş verileri karşılaştırma için temel olarak kullanabilirsiniz. Bütçe planında geçmiş verileri değiştiremezsiniz ve plan onaylı bir iş akışı durumuna ayarlanır. Ancak, plandaki diğer senaryoları değiştirmeniz gerekirse, durumu sıfırlayabilirsiniz.

Sayfanın üstündeki **Toplama göre toplam** alanı da kullanılan tarihi belirler. Bu alan tutarları toplar ve yürürlük tarihini isteğe bağlı olarak mali yılın veya mali dönemin ilk gününe ayarlar. 

<strong>Hedef</strong> öğesindeki alanların çoğu seçtiğiniz eyleme bağlı olarak düzenlenebilir veya salt okunur olabilir. Yeni bir bütçe planı oluşturmaktan mevcut bir planı güncellemeye geçtiğinizde, **Bütçe planı adı** kullanılamaz olur ve mevcut bir planı seçmekle ilgili alanlar kullanılabilir hale gelir. Hem **Hedef** öğesinde hem de **Kaynak** öğesinde, **Genel muhasebe** alanı her zaman kullanılamaz, çünkü değer seçili bütçe planlama süreci ile belirlenir. 

**Bütçe sınıfı** alanı size bütçe planı satırlarını masraf hareketleri veya gelir hareketleri olarak ayarlama olanağı sağlar. Genellikle gelir hareketleri bir genel muhasebe hesabına geçirilir ve bu nedenle negatif tutarlar olarak saklanır. Genellikle, bu hareketler bütçe planında da negatif tutarlar olarak görünür. Ancak, bütçe sınıfını plan düzeninde bir alan olarak ekleyerek, gelirin pozitif tutarlar olarak görünmesini sağlayabilirsiniz.

### <a name="generation-rules"></a>Oluşturma kuralları

Üç alan ek işlevsellik sağlar: **Faktör**, **Minimum** ve **Yuvarlama** **kuralı**. 

**Faktör** alanındaki değer, bütçe planındaki tutarı ayarlamak için kaynak tutarı ile çarpılır. Bütçe planı satırları oluşturduğunuzda, ayarlamalar yapabilirsiniz. Örneğin, yüzde 3'lük bir artış için **1,03** girebilirsiniz. Faktör pozitif bir sayı olmalıdır. 

**Minimum** alanı size bir bütçe planı satırı oluşturmak için eşik tutarını belirleme olanağı sağlar. Kaynak tutarı bu sayıdan az ise, bütçe planı satırı oluşturulmaz. Bir **0,00** değeri, tüm tutarlara izin verir ancak satırları pozitif tutarlara kısıtlamaz. (Pozitif tutarlara değer kısıtlama satırları yok. Negatif tutarlar her zaman dahildir ve genellikle alacak girişlerini temsil eder.)

**Yuvarlama kuralı** alanı oluşturulan bütçe planı satırlarının kesinliğini ayarlamanızı sağlar. Tutarları para biriminin en yakın 1,00, 10,00, 100,00 vb değerlerine yuvarlayabilirsiniz.

## <a name="notes-for-specific-processes"></a>Belirli işlemler için Notlar
### <a name="generate-budget-plan-from-general-ledger"></a>Genel muhasebeden bütçe planı oluştur

Genel muhasebe verilerinden bir bütçe planı oluşturduğunuzda, **Geçmiş** seçeneği **Hayır** olarak ayarlanmış ise, **Toplama göre toplam** alanını **Mali yıl** olarak ayarlamanız gerekir. Kaynaktaki dönemler ve tarihler hedef tarihlerdeki dönemlerle eşleşmeyebilir. İşlemin bu değerleri eşleştirmek için güvenilir bir yolu olmadığı için, işlemi yılın ilk günü olarak sınırlamanız gerekir. 

Hedefte, **Bütçe sınıfı** alanı **Gider** veya **Gelir** olarak ayarlanır. Bu ayar, bir satırdaki ana hesap **Gelir** veya **Gider** türü olmadığında, oluşturulan satırlar için **Bütçe türü** özniteliğini seçmek için kullanılır.

### <a name="generate-budget-plan-from-fixed-assets"></a>Sabit kıymetlerden bütçe planı oluştur

**Sabit kıymetlerden bütçe planı oluştur** işleminde döneme veya güne göre toplam alma seçeneği yoktur. Bir planı tarihsel olarak ayarlamak için bir seçenek yoktur. Bu periyodik işlemi, sabit varlıklar için öngörülen hareketleri bütçe planlamanıza dahil etmek için kullanabilirsiniz.

### <a name="generate-budget-plan-from-forecast-positions"></a>Tahmin konumlarından bütçe planı oluştur

**Tahmin konumlarından bütçe planı oluştur** işlemi, kaynak tahmin konumunu bütçe plan satırına atar. Tahmin konumunu bütçe planı düzeninde bir satır olarak eklemek veya **Bütçe planı satırları** sorgulamasını kullanmak suretiyle konumu görüntüleyebilirsiniz. Tahmin konumunun bütçe planı satırlarına atanmasını istemiyorsanız, **Konumu bütçe planı satırına ekle** seçeneğini **Hayır** olarak ayarlayın.

Bütçe planındaki satırlar genel muhasebe hesabı ve konumuna göre toplanır. Ancak, satırların yalnızca genel muhasebe hesabına göre toplanması için konum numarasını hariç bırakabilirsiniz. **Hedef** öğesinde, **Konumu bütçe planına ekle** seçeneğini **Hayır** olarak ayarlayın.

**Bütçe planı FTE senaryosu** alanında, bütçe planında tam zamanlı eşdeğerlerin (FTE'ler) sayısını eklemek için bir senaryo seçebilirsiniz. Bu alan, hedef bütçe plan düzeninde bulunan miktar türü senaryolar ile sınırlıdır. Bir FTE senaryosu seçerseniz, ayrıca FTE ana hesabını da seçmeniz gerekir. Bu hesap miktar bütçe planı satırları oluşturmak için kullanılır. 

Kaynakta seçilen bütçe planlama süreci ve bütçe planı senaryosu, hedef senaryo bütçe planlama sürecini ve senaryosunu ayarlar. Bu öznitelikler tahmin konumlarına atandığı için, bütçe planı ile eşleşmeleri gerekir. Bu nedenle, bu öznitelikler hedefte değiştirilemez.

### <a name="generate-budget-plan-from-project-forecasts"></a>Proje tahminlerinden bütçe planı oluştur

**Proje tahminlerinden bütçe planı oluştur** işleminde, **Tahmin konumlarından bütçe planı oluştur** işlemi gibi, bir miktar senaryosuna proje miktarları (saatler, giderler ve öğeler) ekleme seçeneği vardır. İki işlemde de bütçe plan düzenindeki sütunlar için benzer filtreler bulunur. 

**Kaynak** öğesinde, **Bildirim ekle** bölümündeki üç seçenek hangi bütçe planı satırlarının oluşturulduğunu belirler. Bu seçenekler, doğrudan proje tahminlerinden bütçe kayıt girişleri oluştururken kullanılabilen seçenekler ile aynıdır. Maliyet ve gelir satırları oluşturmak için, **Kâr ve zarar** seçeneğini **Evet** olarak ayarlayın. Süren iş girişleri oluşturmak için, **Süren İş** seçeneğini **Evet** olarak ayarlayın. Saat hareketlerine ilişkin bordro mahsup hesap satırları oluşturmak için **Bordro tahsisatı** seçeneğini **Evet** olarak ayarlayın. 

**Bütçe sınıfı** alanı yoktur, çünkü bütçe sınıfı (**Gider** veya **Gelir**) kaynak tarafından belirlenir. 

Proje bütçelerini, proje bütçe tutarlarını içeren tahmin modelini seçerek, bir kaynak olarak kullanabilirsiniz. Proje bütçelerinin onaylanır onaylanmaz proje tahmin girişleri oluşturduğunu unutmayın.

Bütçe planı satırlarına ilişkin olarak yalnızca maliyetleri veya gelirleri seçmek için, <strong>Bütçe güncelleştirmeleri: Tutar türü = Maliyet</strong> seçeneğini seçmek üzere filtreyi kullanın. Yalnızca bir tahmin türü seçmek için, <strong>Bütçe güncelleştirmeleri: Hareket türü = *xxx</strong>* seçeneğini seçmek üzere filtreyi kullanın. 

Bir bütçe planı senaryosu oluşturmak için yalnızca bir tahmin modeli kullanılabilir. Bir tahmin modeli sürecini yürütüyorsanız ve daha sonra güncelleştirme yapıp başka bir model belirlemeye çalışırsanız, aynı proje ve genel muhasebe hesapları geçerli olduğu takdirde, ilk modelin üzerine yazılacaktır. Birden fazla tahmin modelinden bir bütçe planı senaryosu oluşturmak için, farklı bütçe planı senaryoları oluşturun ve bunları başka bir senaryoda birbirine eklemek için tahsisat seçeneklerini kullanın. 

**Proje tahminlerinden bütçe planı oluştur** işlemi de kaynak projeyi bütçe planı satırına atar.

### <a name="generate-budget-plan-from-supply-forecast"></a>Tedarik tahmininden bütçe planı oluştur

**Tedarik tahmininden bütçe planı oluştur** işlemindeki kaynak filtre seçenekleri, işlem ve işlev arasındaki benzerliklerden dolayı **Satınalma bütçesini genel muhasebeye aktar** işlevindeki seçeneklerden sonra modellenmiştir.

### <a name="generate-budget-plan-from-demand-forecast"></a>Talep tahmininden bütçe planı oluştur

**Talep tahmininden bütçe planı oluştur** işleminde, bütçe planında gelir satırları oluşturmak için **Satış siparişi** seçeneğini **Evet** olarak; gider satırları oluşturmak için **Tüketim** seçeneğini **Evet** olarak; veya her iki seçeneği **Evet** olarak ayarlayabilirsiniz.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Bütçe kaydı girişlerinden bütçe planı oluşturma

**Bütçe kayıt girişlerinden bütçe planı oluştur** işleminde, kaynak bir alt model, bir bütçe kodu ve bir giriş numarası belirtmelidir. Diğer bir deyişle, bir kerede yalnızca bir bütçe kayıt girişi için bütçe planı satırları oluşturabilirsiniz. İşlemi her kaynak girişi için bir kez yürüterek, aynı bütçe planında ilave girişler kullanabilirsiniz.

### <a name="generate-budget-plan-from-budget-plan"></a>Bütçe planından bütçe planı oluştur

**Bütçe planından bütçe planı oluştur** işleminde, **Hedef** öğesindeki ilave seçenekler kümesi, yeni mali boyutlar atamanıza olanak sağlar. Mali boyut seçili ise, bu değer tüm bütçe planı satırları için kullanılacaktır. Bu nedenle, bir bütçe planını diğer bütçe planları için temel olarak kullanabilir, aynı zamanda, örneğin, farklı bir departman veya maliyet merkezini yeni bütçe planlarına atayabilirsiniz.

## <a name="looking-back-from-the-budget-plan"></a>Bütçe planından geriye bakış
### <a name="budget-plans-by-dimension-set-inquiry"></a>Boyut kümesine göre bütçe planları sorgulaması

**Boyut kümesine göre bütçe planları** sorgulaması bütçe planı verilerinin kaynağını belirlemeye yardımcı olması için bir sorgu yürütmenize olanak sağlayan çeşitli seçenekler içerir. 

Bir satırı seçin ve **Bütçe planı satırları** sorgulamasını çalıştırmak için **Bütçe planı satırları** düğmesine tıklayın. Sonuçları seçili satırın boyut değerleri için filtrelenir. Daha sonra ek parametreler uygulayabilirsiniz. 

Bu sorgulamaları yürütmek için **Tedarik tahmini** ve **Talep tahmini** düğmelerini kullanın. Her iki durumda da, sorgulama bütçe planı satırları oluşturmuş olabilecek tahmin satırlarını arar. 

Mevcut ek raporlar **Bütçe planına göre tahmin konumları** raporunu içerir. Bu rapor bilhassa bir konumun bütçe planlarına doğru şekilde tahsis edilip edilmediğini belirlemek istediğinizde yararlıdır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]