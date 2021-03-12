---
title: Pozisyon tahmini
description: Çalışanlar ile ilgili giderler sıklıkla bir kuruluşun maliyetlerinin büyük bir kısmını teşkil eder. Pozisyon tahmini bu giderleri planlamanızı ve bunları bütçe planlamasına dahil etmenizi sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3452b38fb9fcfc8f4f38e74a8f9c36789110e3a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985523"
---
# <a name="position-forecasting"></a>Pozisyon tahmini

[!include [banner](../includes/banner.md)]

Çalışanlar ile ilgili giderler sıklıkla bir kuruluşun maliyetlerinin büyük bir kısmını teşkil eder. Pozisyon tahmini bu giderleri planlamanızı ve bunları bütçe planlamasına dahil etmenizi sağlar.

## <a name="position-forecasting-in-budget-planning"></a>Bütçe planlamada pozisyon tahmini

[![Pozisyon tahmini bileşenleri](./media/graphic-top.png)](./media/graphic-top.png) 

Pozisyon tahmini, pozisyon giderleri için doğru bütçe tutarlarını sağlamak amacıyla üç ana bileşenden yararlanır. Bu tutarlar, daha sonra bütçe hesaplamaları için bir bütçe planı haline getirilebilir. 

Birincil bileşen, tek bir pozisyonla ilgili tüm maliyet verilerini temsil eden **tahmin pozisyonudur**. Her sürüme farklı bir bütçe planı senaryosu atayarak bir tahmin pozisyonunun farklı sürümlerini oluşturabilirsiniz. Birden çok sürüm, bütçeleme için yinelemeli bir yaklaşım olanağı sunar ve "ne yapmalı" senaryolarını karşılaştırmanızı sağlar. Her tahmin pozisyonunun İnsan Kaynakları'nda ilgili bir pozisyonu vardır.

**Bütçe maliyet öğesi**, temel ödeme, işveren tarafından ödenen sağlık sigortası, cep telefonu tahsisatları vb. gibi bir pozisyonla ilişkilendirilen belli bir maliyeti ifade eden bir ayar bileşenidir. Bütçe maliyet öğesi, maliyet ve hesaplama seçenekleri için kullanılan ana hesabı içerir. Her bir bütçe maliyet öğesine birden çok tahmin pozisyonu atanabilir. 

**Ücret grubu** benzer ödeme özelliklerine sahip pozisyonlara bir bütçe maliyet öğeleri ve ödeme hesaplamaları kümesini uygulamak için kullanılan isteğe bağlı bir ayar bileşenidir. Bir ücret grubu, ödeme oranları ücret kılavuzu içerebilir. Grup bir tahmin pozisyonuna atanmışsa, kılavuzdaki bir düzey ve adım tahmin pozisyonunun kazançlarını atayabilir. Maliyet öğeleri kümesi otomatik olarak eklenir.

### <a name="position-forecasting-processes"></a>Pozisyon tahmini işlemleri

[![Pozisyon tahmini işlemlerinin gösterimi](./media/graphic1b.png)](./media/graphic1b.png) 

Tipik bir pozisyon tahmin işleminde, öncelikle ayar bileşenlerini (bütçe maliyet öğeleri ve ücret grupları) oluşturursunuz. Tahmin pozisyonları daha sonra mevcut pozisyonlar esas alınarak oluşturulur. Sonra ayarlamalar yapabilirsiniz. Örneğin, pozisyon ekleyebilir veya sonlandırabilir, ödeme oranlarını ve kazanç maliyetlerini değiştirebilir ve ücret zammı ekleyebilirsiniz. Farklı bütçeleme senaryoları arasındaki karşılaştırmaları kolaylaştırmak için birden çok tahmin pozisyonu sürümü oluşturabilirsiniz. Ardından, tahmin pozisyonlarını bütçe planlarına dahil edebilir ve tahmin pozisyonlarından maliyetleri bütçe planı satırları olarak ekleyebilirsiniz.

Bütçe planları revize edilirken ek tahmin pozisyonu sürümleri oluşturabilirsiniz. Bu yeni sürümler, revizyonlar için bir temel oluşturur.

## <a name="position-forecasting-setup"></a>Pozisyon tahmini ayarlama
[![Ayarı vurgulayan çizim](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Bütçe maliyet öğeleri

Bütçe maliyeti öğeleri bir tahmin pozisyonu için maliyet ayrıntılarını tanımlamada kullanılır. Bu ayrıntılar maliyet türünü, maliyeti hesaplama şeklini ve tahmin pozisyonu bir bütçe planına dahil edildiğinde maliyetin birden çok tarihe tahsis edilip edilmeyeceğini içerir. 

Belirli alanlar bütçe maliyet öğesi davranışını tanımlar. Her bütçe maliyet öğesine **Gelir**, **Kazanç**, **Vergiler** veya **Diğer** şeklinde bir bütçe maliyet türü atanır. Bütçe maliyet türleri temel olarak toplamları hesaplamak için kullanılır. **Tahmin pozisyonunu geçersiz kılma** değeri öğedeki tutarların tahmin pozisyonunda değiştirilip değiştirilemeyeceğini belirtir. **Tahsisat yöntemi** alanı bir tahmin pozisyonu bir bütçe planına eklendiğinde kullanılır. Maliyet tutarını aylık, üç aylık, haftalık veya iki haftalık temelinde farklı tarihleri bulunan ayrı bütçe planı satırlarına bölebilirsiniz. Bir başlangıç tarihi seçerek, maliyeti, tahmin pozisyonunda ayarlanan başlangıç tarihinde tek bir tutar olarak atarsınız. 

Bütçe maliyeti öğesinin maliyet tutarının hesaplamasında, aynı maliyet öğesinin farklı dönemlerde kullanılmasını sağlayacak şekilde geçerlilik tarihleri kullanılır. Tek bir ana hesap, her dönemde, maliyet tutarını belirten bir yüzde veya yıllık tutarı ile birlikte atanır. Bütçe maliyet öğesi, diğer maliyet öğelerinin yüzdesini veya yıllık bir tutarı kullanabilir, ancak ikisini birden kullanamaz. Ayrıca, bir yıllık sınırı da belirtebilirsiniz. 

Maliyet öğesi yüzdeye dayalı ise, hesaplama için temel olarak kullanılan bütçe maliyeti öğelerini belirtmeniz gerekir.

**Örnek** 

Jodi'nin kuruluşu, bir çalışanın temel ödemesinin yüzde 5'i kadar bir eğitim tahsisatı sağlıyor. Jodi bu maliyet için bir bütçe maliyet öğesi oluşturmak istiyor. Yeni bir bütçe maliyet öğesi oluşturuyor ve **Kazanç** bütçe maliyet türünü atıyor.

Jodi yöneticilerin kazanç miktarını değiştirmesini istemiyor. Bu nedenle, **Tahmin pozisyonunu geçersiz kılma** alanında **Maliyet değişikliklerine izin verme** seçeneğini seçiyor. Kuruluş bu maliyetin her aya eşit olarak atanmasını istiyor. Bu nedenle, Jodi **Tahsisat yöntemi** alanında **Üç aylık** seçeneğini seçiyor. 

Ardından, Jodi maliyet hesaplama satırı ekliyor, tarihleri ve bir ana hesabı ayarlıyor ve yüzde olarak **5,00** değerini giriyor. Kuruluşunda, bu kazanç için yılda 5,000 $'lık bir kapasite vardır. Bu nedenle, Jodi bu tutarı yıllık sınır olarak giriyor. 

Son olarak, Jodi temel ödeme için hesaplama tabanları olarak kullanılan tüm gelir maliyet öğelerini ekliyor. Bütçe maliyet öğesi artık kullanılmaya hazırdır.

### <a name="compensation-groups"></a>Tazminat grupları

Ücret grupları, benzer ücret özniteliklere sahip tahmin pozisyonunu gruplamak için kullanılabilir. Bunlar, tahmin pozisyonun kazançlarını ve yıllık artışlarını tanımlamak için ve genel bütçe maliyeti öğeler kümesi atamak için de kullanılabilir. 

Ücret gruplarının temel bir işlevi bir tahmin pozisyonuna bir bütçe maliyet öğeleri kümesi atamaktır. Bu nedenle, ücret grupları kazanç planları ve vergiler gibi ortak maliyetler eklemek için kullanılabilir. Tahmin pozisyonu oluşturan bir yönetici eklenmesi gereken tüm maliyet öğelerini bilmek zorunda değildir. Bunun yerine, ücret grubu seçildiğinde maliyet öğeleri eklenebilir. Öğeler **Bütçe maliyet öğeleri** öğesindeki ücret grubu ayarına eklenir. 

Ücret grupları bir tahmin pozisyonuna ait kazanç oranlarını da belirleyebilir. Tahmin pozisyonu kazançlarını hesaplamak için bir grubu saat başı temelinde veya yıllık ücret temelinde ayarlayabilirsiniz. **Ücret oranı tabloları** öğesinde, ödeme oranları ücret kılavuzu, atanmış bir düzey ve adım temelinde bir tahmin pozisyonuna eklenen kazançları belirler. Bu kılavuzlar İnsan Kaynakları'ndaki mevcut ücret kılavuzlarına dayanabilir. Alternatif olarak, bütçe planlama için yeni ücret kılavuzları oluşturabilirsiniz. 

Ücret oranı tablolarındaki geçerlilik tarihleri ve bitiş tarihleri ödeme oranlarını istediğiniz tarihte değiştirmenizi sağlar. Bu özellik, bir pazarlık biriminin bir bütçe döngüsünün ortasında geniş kapsamlı maaş zammı için görüşmelerde bulunduğu zaman yararlıdır. Bu durumda, var olan bir tablonun sona erme tarihini oran değişikliği tarihinden önceki güne değiştirin ve yeni tarihte başlayan yeni bir fiyatı tablosu ekleyin. Yeni bir oran tablosu oluşturduğunuzda **Mevcut bir kılavuzdan yeni bir tazminat kılavuzu oluştur**'u seçerseniz, İnsan Kaynaklarından var olan bir fiyat tablosunu seçebilirsiniz. Oluşturulan oran tablosunda, **Toplu Değişiklik** seçeneği, kılavuzdaki tüm oranlara bir yüzde veya sabit tutar artışı veya azalması uygulamanızı sağlar. 

Ücret grubundaki **Artış planı** ve **Artış tarihi** alanları, pozisyonlar bir adımdan diğerine geçtiği için ödeme artışları oluşturmanız gerektiğinde kullanılır. Bir yıllık ödeme artışı tipik bir senaryodur. Artış planı, adım artışı için pozisyonun yıldönümü tarihinin mi, yoksa tek bir ortak tarihin mi kullanılacağını belirler. Artış planı ücret grubundaki tüm tahmin pozisyonlarına uygulanır. 

Ücret grubunda seçilen kazanç maliyet öğesi, kendi temel ödemeleri ve her adım artışı dahil olmak üzere, gruptaki tahmin pozisyonları için kazanç oluşturduğunuzda kullanılır. **Ücret sabit planı** alanı ücret grubunu İnsan kaynaklarındaki bir sabit ücret planına bağlar. Bu bağlantı bir çalışanın sabit ücret bilgilerini bir tahmin pozisyonuna atar ve böylece bütçe planlamasını daha doğru hale getirebilir. Ücret grubu için ücret kılavuzunun (düzeyler ve adımlar) yapısının sabit ücret planının yapısıyla uyuşması gerektiğini unutmayın. Aksi takdirde, sistem ücret grubu ile sabit ücret planını doğru şekilde bağlayamazsınız.

## <a name="creating-forecast-positions"></a>Tahmin pozisyonları oluşturma
[!["Tahmin pozisyonları oluşturma"yı vurgulayan çizim](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Mevcut pozisyonlar için tahmin pozisyonları oluşturma

En doğru bütçe planlama için pozisyonun o anda doldurulmuş veya boş olmasından bağımsız olarak mevcut pozisyonlardan ayrıntılar ile tahmin pozisyonları oluşturabilirsiniz. 

**Mevcut pozisyonları ekle** işlevi bir kuruluşa ait tüm pozisyonları görüntüler. **Başlangıç** tarihini ayarlayarak, pozisyonlar listesini geçmişteki veya daha yaygın olarak gelecekte bir tarihteki mevcut pozisyonları içerecek şekilde değiştirebilirsiniz (örneğin, bir sonraki bütçe döngüsünün başlangıcı). Bir bütçe planlama süreci ve bütçe planı senaryosu seçin, listede pozisyonları seçin ve seçilen pozisyonlar için tahmin pozisyonları oluşturmak için **Tamam** düğmesine tıklayın. Bir bütçe planlama süreci ve senaryosundaki her bir mevcut pozisyon için sadece bir tahmin pozisyonu oluşturabileceğinizi unutmayın. Ancak, farklı bütçe planı senaryoları atayarak ek sürümler oluşturabilirsiniz. 

Bütçe maliyet öğeleri İnsan kaynaklarındaki pozisyona atanmışsa, bu bütçe maliyet öğeleri de tahmin pozisyonuna atanır ve varsayılan tutarları kullanır. Bir çalışan atanmışsa, tahmin pozisyonundaki **Atanan çalışan** alanı, pozisyona atanan o çalışanın adına ayarlanır. Bu alan, basit bir metin alanıdır. Doğrudan bağlantı oluşturulmaz. 

Bütçe maliyet öğesi seçili ise, atanan çalışanın bir sabit ücret planı olması koşuluyla, sabit ücret yıllık tutarı seçili maliyet öğesi kullanılarak tahmin pozisyonuna atanır. Çalışanın sabit ücret planı yoksa veya hiçbir çalışan atanmamışsa, varsayılan tutar bütçe maliyet öğesi için kullanılır. 

**Bir ücret grubu ata** seçeneği **Evet** olarak ayarlanmış ise, pozisyona atanmış çalışanın bir ücret grubuna bağlı olan adım temelli bir sabit ücret planının olması durumunda (daha önce tarif edilen şekilde), çalışana ait düzey ve adım ücret grubu ile birlikte tahmin pozisyonuna atanır. Ücret grubundan kazanç bütçe maliyet öğesi, tahmin pozisyonuna eklenir ve ücret grubundan düzey ve adımdaki ödeme oranı kullanılır. 

**Bir ücret grubu ata** seçeneği ayarı, **Bütçe maliyet öğesi atama** ayarından daha önceliklidir. Aynı anda iki ayar kullanılabilir. 

[!["Ücret grubu atama" grafiği](./media/graphic4.png)](./media/graphic4.png) 

Diğer seçenek yıldönümü tarihi atamaktır. Daha sonra, atanan çalışandan seçilen tarih (ayarlanan başlangıç tarihi, çalışan başlangıç tarihi, işe alma başlangıç tarihi veya kıdemlilik tarihi) tahmin pozisyonunun yıldönümü tarihi olarak ayarlanır ve bilgilendirme amacıyla ve ödeme artışları oluşturulduğunda kullanılır.

### <a name="creating-new-forecast-positions"></a>Yeni tahmin pozisyonları oluşturma

Yeni tahmin pozisyonlarını iki şekilde oluşturabilirsiniz: mevcut bir tahmin pozisyonunu kopyalayarak ve tamamen yeni bir tahmin pozisyonu oluşturarak. 

Bir tahmin pozisyonu seçildiğinde, **Önerilen** şeklindeki tahmin durumuna sahip yeni bir tahmin pozisyonu oluşturmak için **Seçilen tahmin pozisyonunu kopyala** seçeneğini seçin. Bu tahmin pozisyonunda, atanmış çalışan ile bütçe maliyet öğelerine ilişkin tüm notlar hariç, kopyalanan tahmin pozisyonu ile aynı verilerin tümü mevcuttur. İlgili bir yeni pozisyonun İnsan kaynakları'nda da oluşturulduğunu unutmayın. Bu pozisyonun bir **Tahmin ile oluşturuldu** tanımı bulunur. 

Ayrıca tamamen yeni bir tahmin pozisyonu da oluşturabilirsiniz. Mevcut bir görevi ve ayrıca bütçe planlama sürecini ve bütçe planı senaryosunu seçin. Ardından eklemek istediğiniz diğer ayrıntıları ekleyebilirsiniz. Bir kez daha, aynı anda İnsan kaynaklarında yeni bir pozisyon oluşturulur.

## <a name="working-with-forecast-positions"></a>Tahmin pozisyonları ile çalışma
[!["Tahmin pozisyonlarını değiştirme"yi vurgulayan çizim](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Bir tahmin pozisyonunun farklı sürümleri

Tahmin pozisyonlarını bütçe döngüsü için bilinen değişiklikleri uygulayacak veya önerilen değişiklikleri modelleyecek şekilde değiştirebilirsiniz. Yaygın bir uygulama, tahmin pozisyonlarına ait bir başlangıç kümesi oluşturmak, bu tahmin pozisyonlarının kopyalarını oluşturmak ve sonra kopyaları farklı değişiklik kümelerini modellemek için kullanmaktır. Kopyalar farklı bir bütçe planı senaryosuna atanır, ancak en azından değişiklikler yapılana kadar, kopyalandıkları tahmin pozisyonları ile özdeştir. Orijinaller ve kopyalar İnsan kaynaklarında aynı pozisyonu paylaşır. 

**Senaryoya kopyala** işlevi bu işlevselliği sağlar. Her İnsan kaynakları pozisyonunun her bütçe planı senaryosunda sadece bir tahmin pozisyonu olabileceğini unutmayın.

### <a name="modifying-forecast-positions"></a>Tahmin pozisyonlarını değiştirme

Tahmin pozisyonlarında yapılan değişiklikler bu tahmin pozisyonları ile sınırlıdır. Değişiklikler İnsan kaynakları'ndaki pozisyon kayıtlarını etkilemez. Değişikliklerin çoğu düzenlenen tahmin pozisyonu ile de sınırlıdır. Diğer bir deyişle, değişiklikler atanan bütçe planlama süreci ve bütçe planı senaryosuna özgüdür. Özel durumlar, işlemler ve senaryolar arasında pozisyon için paylaşılan alanlarda yapılan değişikliklerdir. Bu alanlar **Mali boyutlar** sekmesinde ve **Genel** sekmesindeki alanları içerir. Bu alanlar değiştirildiğinde, yeni değerler tüm bütçe planlama senaryolarındaki konuma uygulanır. Böylece, bu alanlar tüm sürümleri hızla güncelleştirmenizi sağlar.

#### <a name="budget-cost-elements"></a>Bütçe maliyet öğeleri

Bütçe maliyet öğeleri bütçe planları için temel bilgileri sağlar: bütçe tutarı ve ana hesap. Bütçe tutarı, bir tahmin pozisyonu bir plana dahil edildiğinde bütçe planına gönderilen tutardır. Bütçe tutarı hesaplanır ve doğrudan değiştirilemez. Bu tutar, yıllık tutar ya da (bütçe maliyet öğesi ayarlamasında tanımlandığı üzere) yıllık tutarın temel öğelerinin yüzde hesabıdır. Tutar daha sonra öğenin tarih aralığındaki (başlangıç tarihinden bitiş tarihine) günlerin sayısı ve ayrıca tahmin pozisyonu için **Tam zamanlı eşdeğer** (FTE) değeri ile çarpılır. 

Örneğin, 100.000'lik bir yıllık tutarı ve **0,50**'lik bir FTE değeri olan, 1 Ocak 2017 ile 30 Haziran 2017 tarihleri arasındaki bir bütçe maliyet öğesi satırı, 100.000 × (181 gün ÷ 365 gün) × 0,50 = 24,794.52 olarak hesaplanır. 

FTE değeri tahmin pozisyonunda değiştirildiğinde bütçe maliyet öğesi satırları yeniden hesaplanmalıdır. Satırlar etkinleştirme tarihleri veya kaldırma tarihleri değiştirildiğinde de yeniden hesaplanmalıdır. Bu tarihlerde yapılan değişiklikler, bütçe maliyet öğesinin başlangıç ve bitiş tarihlerinin güncellenmesine yol açar ve bu tarihlerin tahmin pozisyonunun tarih aralığında olması gerekir. Yeniden hesaplama gerektiğinde, **Yeniden hesapla** düğmesi kullanılabilir olur ve bir "Hesaplama gerekli" iletisi görüntülenir. Yeniden hesaplama, bir bütçe maliyet öğesi eklemeniz veya kaldırmanız durumunda da gereklidir.

**Örnek** 

Kuruluş bir muhasebeci pozisyonunun maliyetini azaltmak için iki seçenek düşünüyor. Birinci seçenek, pozisyonu yıl bitmeden kaldırmaktır. Diğer seçenek, pozisyonu tüm yıl boyunca yarı zamanlı olarak değiştirmektir. Brad bir başlangıç senaryosunda mevcut muhasebeci pozisyonu için bir tahmin pozisyonu oluşturdu. Bu başlangıç tahmin senaryosunu A senaryosuna kopyalayıp kaldırma tarihini 31 Mayıs olarak ayarladı ve yeniden hesapladı. Sonra Brad başlangıç tahmin pozisyonunu B senaryosuna kopyalayıp FTE değerini **0,50** olarak değiştirdi ve yeniden hesapladı. Brad'in şimdi üç sürümü ve her bir sürümün kendi seçenekleri ile uyumlu maliyet toplamları vardır.

#### <a name="assigning-a-compensation-group"></a>Bir ücret grubu atama

İlk olarak bir ücret grubunu bir tahmin pozisyonuna atadığınızda, ücret grubundan varsayılan bütçe maliyet öğeleri eklenir. Maliyet öğeleri halihazırda tahmin pozisyonuna atanmışsa, bu maliyet öğeleri kalır. Ücret grubu halihazırda atanmışsa ve değiştiriliyorsa, mevcut bütçe maliyet öğeleri kaldırılır ve ücret grubundan küme ile değiştirilir. 

Bir ücret düzeyi ve adım seçtiğinizde, (ücret grubunda tanımlandığı gibi) bir kazanç bütçe maliyet öğesi eklenir. Yıllık tutar, seçilen düzey ve adımdaki oran ile ücret grubundaki yıllık saatler (veya yıllık temelli maaş için düzey ve adımdaki tam tutar) kullanılarak hesaplanır. Bir kez daha, bu tutar maliyet öğe satırındaki tarih aralığı ve tahmin pozisyonunun FTE değeri ile çarpılır.

#### <a name="generating-increases"></a>Artışlar oluşturma

Yıllık artışlar (takvim yılı başına bir), atanmış bir adım temelli ücret grubu olan tahmin pozisyonları için otomatik olarak oluşturulabilir. Bir sonraki en yüksek adımda bir kazanç bütçe maliyet öğesi eklemek için **Artış oluştur** seçeneğine tıklayın. Yeni kazanç bütçe maliyeti öğesinin başlangıç tarihi, tahmin pozisyonunda gösterilen planlanmış artış tarihidir. Bu tarih, ücret grubundan iki yoldan biri ile ayarlanır. Ücret grubunun artış planı **Ortak tarih** olarak ayarlanırsa, artış tarihi ücret grubunda belirtilir. Artış planı **Yıldönümü tarihi** olarak ayarlanırsa, tahmin pozisyonundaki yıldönümü tarihi alanı kullanılır ve bütçe döngüsü yıl boyunca sağlanır. Bir bütçe döngüsünde birden çok takvim yılı varsa, birden çok artış eklenir. 

Geçerli kazanç bütçe maliyet öğesinin bitiş tarihi artış tarihinden önceki gün olarak güncelleştirilir. Yeniden hesaplama işlemi, artışlar oluşturulduğunda otomatik olarak kullanılır. Bu nedenle, el ile yeniden hesaplamak zorunda değilsiniz. 

**Artış oluştur** seçeneğine ikinci kez tıklarsanız, işlem yeniden yürütülür, ancak daha fazla kayıt eklemez. Takvim yılı başına yalnızca bir artış oluşturulur.

#### <a name="changes-from-other-pages"></a>Diğer sayfalardan değişiklikler

Tahmin pozisyonlarına yapılan güncelleştirmeler, bütçe maliyet öğesi ve ücret grubu ayar sayfaları gibi diğer alanlardan da gelebilir. Tahmin pozisyonlarını toplu güncelleştirme işlemini kullanarak da değiştirebilirsiniz. 

**Bütçe maliyet öğesi** ayar sayfasında iki seçenek bulunur: **Pozisyonlara ekle** ve **Pozisyonları güncelleştir**. **Pozisyonlara ekle** seçeneği, bütçe maliyet öğesini seçilen tahmin pozisyonlarına ekler. Öğe halihazırda bir tahmin pozisyonuna atanmışsa, o tahmin pozisyonu atlanır. **Pozisyonları güncelleştir** seçeneği mevcut değerleri (ana hesap, yüzde, yıllık tutar, vb..) seçilen tahmin pozisyonlarına uygular. 

Her işlemin, tahmin pozisyonlarını seçebileceğiniz benzer bir sayfası bulunur. **Pozisyonlara ekle** sayfası seçim için kullanılabilir olan tüm tahmin pozisyonlarını, **Pozisyonları güncelle** sayfası sadece halihazırda atanmış bütçe maliyet öğesi bulunan tahmin pozisyonlarını gösterir. (Bu nedenle, **Pozisyonları güncelleştir** sayfası hangi tahmin pozisyonlarına zaten maliyet öğesi eklendiğini bulmak için bir yol sunar.) Güncelleştirmeye dahil etmek için tahmin pozisyonlarını üst kılavuzdan alt kılavuza taşıyın. 

**Maliyet hesaplaması** öğesindeki **Tarihleri değiştir** işlevinin tahmin pozisyonlarındaki bütçe maliyet öğesinin başlangıç ve bitiş tarihlerini hemen değiştirdiğini unutmayın. Hiçbir seçim seçeneği kullanılamaz. 

**Ücret grubu** sayfasında, **Pozisyon oranlarını güncelleştir** işlevi, mevcut ücret oranı tablo oranlarını gruba atanan tahmin pozisyonlarına uygular. Oranları güncelleştirilir ve ek maliyet öğesi satırları her yeni oran tablo satırları için (tarihler temel alınarak) eklenir. Ancak, bütçe maliyet öğeleri ve artış tarihleri güncelleştirilmez. Hangi bütçe planlama süreci ve bütçe planı senaryosunun güncelleştirileceğini seçebilirsiniz. Bu nedenle, bir senaryoyu güncelleştirebilirsiniz, ancak diğer senaryoları karşılaştırma için değiştirmeden bırakın. 

Tahmin pozisyonlarını seçip, ardından **Toplu güncelleştirme** seçeneğine tıklayarak, aynı anda birden fazla tahmin pozisyonunu ekleyebilir veya değiştirebilirsiniz. Pek çok seçenek kullanılabilir. **Mali boyutlar** öğesindeki bir seçenek, diğerlerinden biraz daha farklıdır ve bütçe maliyet öğeleri ile ilgilidir. Bütçe maliyet öğelerini, **Bütçe varsayılanları** seçeneğini **Evet** olarak ayarlayarak ekleyebilirsiniz. Hiçbir bütçe maliyet öğesi seçilmez, ancak **Bütçe varsayılanları** **Evet** olarak ayarlanırsa, halihazırda atanmış olan tüm bütçe maliyet öğeleri kaldırılır. 

Yeniden hesaplama işlemi değiştirilen tüm tahmin pozisyonlarında otomatik olarak kullanılır.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Tahmin pozisyonlarını bütçe planlarına getirme

[!["Bütçe planına ekleme"yi vurgulayan çizim](./media/graphic6-1024x327.png)](./media/graphic6.png)

Tahmin pozisyonları oluşturma ve değiştirmenin amacı bunları bütçe planlarına eklemektir, böylece bütçe planları en doğru bütçe tutarlarını içerir. Tahmin pozisyonlarını bütçe planlarına eklemek için iki yöntem vardır. Bütçe planında oluşturma işlemini veya seçim işlemini kullanabilirsiniz.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Tahmin pozisyonlarından bütçe planı oluşturma

**Bütçe planını tahmin pozisyonlarından oluştur** işlevi, bütçe planlarını tahmin pozisyonlarından bütçe tutarları ve FTE sayılarına sahip olacakları şekilde oluşturur veya güncelleştirir. Tahmin pozisyonunda bütçe tutarları, bütçe planı satır tutarları olur ve mali boyut değerleri ve geçerlilik tarihi ile toplanır. Oluşturma işlemi, kaynak tahmin pozisyonunu bütçe plan satırına atar. Pozisyonu görüntülemek için, tahmin pozisyonunu bütçe planı düzeninde bir satır olarak ekleyebilir veya **Bütçe planı satırları** sorgulamasını kullanabilirsiniz. Bu atamayı atlamak için, **Pozisyonu bütçe planına dahil et** seçeneğini **Hayır** olarak ayarlayın. 

FTE'lerin sayısını bütçe planına eklemek için bir bütçe planı FTE senaryosu seçebilirsiniz. Yalnızca, hedef bütçe planının düzenine eklenen miktar türü senaryolarını seçebilirsiniz. Bir FTE senaryosu seçtiğinizde, ayrıca bir FTE ana hesabı da belirtmeniz gerekir. Bu hesap miktar bütçe planı satırları oluşturmak için kullanılır. 

Kaynakta seçilen bütçe planlama süreci ve bütçe planı senaryosu, hedef senaryo bütçe planlama sürecini ve senaryosunu belirler. Bu öznitelikler tahmin pozisyonlarına atandığı için, bunların bütçe planı ile eşleşmeleri gerekir. Bu nedenle, öznitelikler hedefte düzenlenemez. 

Diğer oluşturma işlemlerinde olduğu gibi, için seçenek kullanılabilir:

-   **Yeni bir bütçe planı oluştur** – **Hedef** bölümünde seçilen özniteliklere sahip yeni bir plan oluşturur.
-   **Mevcut bütçe planı senaryosunu değiştir** – Seçilen bütçe planı senaryosundaki hedef bütçe planında bulunan tüm verileri siler ve seçilen tahmin pozisyonu verilerine sahip yeni satırlar oluşturur.
-   **Mevcut bütçe planı senaryosunu güncelleştir ve yeni veriler ekle** – Hedef planda kaynak satırlarla eşleşen mevcut satırları günceller ve ayrıca yeni veriler için yeni satırlar ekler. Eşleştirme, genel muhasebe hesabına, tarihe, bütçe sınıfına ve tahmin pozisyonu gibi diğer değerlere dayanır. Kaynak konum numarasıyla eşleşen bir konum numarası olan tüm satırlar, kaynaktan yeni satırlar ile değiştirilir.

### <a name="selecting-forecast-positions"></a>Tahmin pozisyonlarını seçme

Ayrıca tahmin pozisyonu bütçe tutarlarını doğrudan bir bütçe planına ekleyebilirsiniz. Dahil edilecek tahmin pozisyonlarını seçmek için, bütçe planı satırlarının üzerindeki **Pozisyonları ekle** işlevini kullanın. 

Kaynak olarak seçebileceğiniz bütçe planı senaryoları, planın düzenine dahil edilen senaryolar ile sınırlıdır. **Hedef** öğesindeki bir seçenek, FTE sayılarını eklemek için FTE senaryosunun ve ana hesabın kullanılabilir olduğunu, ancak gerekli olmadığını belirtmenizi sağlar. 

Bu seçim işlemi, bir oluşturma işlemi için **Mevcut bütçe planı senaryosunu güncelleştir ve yeni veriler ekle** seçeneği gibi hareket eder. Tahmin pozisyonunun eklendiği tüm mevcut bütçe planı satırları kaldırılır ve tahmin pozisyonunun geçerli durumuna dayanılarak yeni satırlar ile değiştirilir.

#### <a name="date-options"></a>Tarih seçenekleri

Hem oluşturma süreci hem de seçim süreci için, bütçe maliyet öğesi satırındaki başlangıç tarihi ilgili bütçe planı satırının geçerlilik tarihini belirler. Bütçe maliyet öğesi ayar sayfasındaki **Tahsisat yöntemi** alanı, tahsisat yöntemini belirtir:

-   **Başlangıç tarihi** – Bütçe maliyet öğesinin başlangıç tarihi bütçe planı satırının geçerlilik tarihi olarak kullanılır.
-   **Aylık** – bütçe tutarı, her ayın ilk günü atanan tipik bir aylık tutar oluşturmaya yönelik tarih aralığındaki ayların sayısına eşit olarak bölünür. İlk dönem kısmi bir ay ise, o aya ait tutar maliyetin o ay aktif olduğu gün sayısı ile çarpılır ve sonuç başlangıç tarihine atanır. Önceki aya ait tutar toplam bütçe tutarı ile diğer tüm ayların toplamı arasındaki farktır. Bu nedenle, yuvarlama önceki aya ait tutarı etkileyebilir.
-   **Üç aylık** – bu yöntem **Aylık** yöntemi ile aynıdır, ancak hesaplamalar üç aylık dönemler için yapılır.
-   **Haftalık** – Mantık **Aylık** ve **Üç aylık** yöntemlerinin mantığına benzer. Bütçe tutarı, her haftanın ilk günü atanan tipik bir haftalık tutar oluşturmaya yönelik tarih aralığındaki haftaların sayısına eşit olarak bölünür. İlk dönem kısmi bir hafta ise, o haftaya ait tutar maliyetin o hafta aktif olduğu gün sayısı ile çarpılır ve sonuç başlangıç tarihine atanır. Önceki haftaya ait tutar toplam bütçe tutarı ile diğer tüm haftaların toplamı arasındaki farktır. Bu nedenle, yuvarlama önceki haftaya ait tutarı etkileyebilir.
-   **İki haftalık** – bu yöntem **Haftalık** yöntemi ile aynıdır, ancak hesaplamalar iki haftalık dönemler için yapılır.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Tahmin pozisyonları olan bütçe planı satırlarını değiştirmek

Bütçe planı satırları, bütçe tutarlarının kaynağını (tahmin pozisyonu numarası) gösterir ancak bağlı değildir. Bu nedenle, tahmin pozisyonlarındaki değişiklikler bütçe planı satırında gösterilmez ve bütçe planı satırındaki değişiklikler tahmin pozisyonunda gösterilir. Bir tahmin pozisyonunu değiştirir ve güncelleştirmeleri bir bütçe planına eklemek isterseniz, tahmin pozisyonunu tekrar plana getirmeniz gerekir. Bununla birlikte, bu işlemin, o tahmin pozisyonunun atandığı tüm satırları kaldıracağını unutmayın. Bu nedenle, bu satırlarda yaptığınız tüm değişiklikler kaldırılır. 

Bir tahmin pozisyonunun hangi bütçe planlarına eklendiğini görmek için, **Bütçe planına göre tahmin pozisyonları** raporu oluşturabilirsiniz. Alternatif olarak, tahmin pozisyonunda, planları görüntülemek için **İlişkilendirilmiş bütçe planları** Bilgi Kutusunu açabilirsiniz.



