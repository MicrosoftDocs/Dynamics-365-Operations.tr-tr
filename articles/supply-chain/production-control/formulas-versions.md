---
title: Formüller ve formül sürümleri
description: Bu konu, formül ve formül versiyonlarının hakkında bilgi sağlar. Malzemeleri, içerikleri ve işlem üretimindeki belirli bir işlemin sonucunu tanımlayan bir formül. Formüller işlem üretiminde ürünleri planlamak ve üretmek için kullanılır.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e5ff5916366f968cbf8dc9a5614466ef89faa92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007182"
---
# <a name="formulas-and-formula-versions"></a>Formüller ve formül sürümleri

[!include [banner](../includes/banner.md)]

Malzemeleri, içerikleri ve işlem üretimindeki belirli bir işlemin sonucunu tanımlayan bir formül. Buna karşılık gelen yol ile birlikte, formül işlem üretimindeki tüm işlemi tanımlar. Formüller işlem üretiminde ürünleri planlamak ve üretmek için kullanılır.

Bir formül, bir formül maddesinden belirli bir miktarda üretmek için gerekli içerikleri ve miktarlarından oluşur. Gerçekleştirdiğiniz göreve bağlı olarak, formül işlevine Stok veya ambar yönetiminden veya Ürün bilgisi yönetiminden erişebilirsiniz.

## <a name="formulas-and-formula-lines"></a>Formüller ve formül satırları
Bir formül, formülü oluşturan malzemeleri tanımlayan bir veya daha fazla formül satırından oluşur. Bir formül satırı Ürün reçetesi (BOM) maddelerini, formül maddelerini, fiili ağırlık maddelerini, satın alınan maddeleri, ortak ürünleri veya yan ürünleri içerebilir. Çoğu madde birden fazla üründe kullanıldığından bir maddeyi birden fazla formülde kullanılabilir.

Bir formül örneği, bir çikolatalı kurabiye reçetesidir. Bu formül için içindekiler birçok satır kullanır; örneğin un, şeker, yumurta, tereyağı ve çikolata parçacıkları gibi. Çikolata parçacıklı kurabiye için formül, diğer tarif türü formüllerde kullanılması olası malzemelere sahiptir. Çikolata parçacıklı kurabiyeler pişirdiğinizde, artıklar kalabilir, örneğin kırıntılar gibi veya kurabiyelerin bazıları az veya çok pişmiş olabilir. Bu öğeler ortak ürün veya yan ürünler olarak ayarlanabilir, üretim işlemlerini bağlı olarak.

Bir formül satırı oluşturduğunuzda, satır türünü, master planlamayı çalıştırdığınızda ve toplu iş emirleri ürettiğinizde sistemin satırı nasıl ele alacağını belirtmek için satır türlerini kullanırsınız. Her satır tipi farklı bir sonuç verir. Aşağıdaki tabloda seçebileceğiniz satır tipleri açıklanmıştır. 

| Satır türü     | Tanım  |
|---------------|--------------|
| Madde          | Madde bir hammadde veya stoktan çekilmiş yarı tamamlanmış madde olduğunda ya da serviste olduğunda **Madde**'yi seçin. |
| Hayali       | Formül satırında bulunan daha alt düzeydeki formül maddelerini açmak istediğinizde **Hayali**'yi seçin. Toplu iş emrini tahmin ettiğinizde ve formül maddeleri açıldığında, bileşen maddeleri toplu iş emrinde formül satırları olarak listelenir. Ayrıca, üretim rotası için karşılık gelen yollar eklenir. Formül maddeleri geçerli konfigürasyon kullanılarak açılır. **Hayali** satır tipini kullandığınızda, farklı formül düzeylerinde oluşan üretim ve ölçüm konfigürasyonlarını işleyebilirsiniz. **Hayali**'yi, **Yayımlanan ürün ayrıntıları** sayfasında **Mühendis** hızlı sekmesi üzerinde seçerseniz ve sonra bu ürünü bir formülde kullanırsanız, formül satırının satır türü **Hayali** olarak değişir. Fiili ağırlık maddesi veya üretim türünün **Orta ürün**, **Yan ürün** veya **Planama maddesi** olduğu maddeler için **Hayali** seçemezsiniz. |
| İlişkilendirilmiş tedarik | Formül satırında bulunan bir içerik için bir toplu iş siparişi, üretim emri, kanban, transfer emri veya satınalma siparişi oluşturmak için **Pegged tedarik**'i seçin. İlgili sipariş, varsayılan sipariş ayarları ve içeriğin üretim türüne dayalı olarak belirlenir ve toplu iş emrini tahmin ettiğinizde oluşturulur. Gerekli içerik miktarları toplu iş emri için rezerve edilir. |
| Satıcı        | Üretim süreci bir alt yüklenici kullanırsa ve alt yüklenici için bir alt üretim veya satın alma siparişi oluşturmak istiyorsanız **Satıcı**'yı seçin. Alt yüklenici tarafından gerçekleştirilen servis veya işin bir formül maddesi veya servis maddesi kullanılarak oluşturulması gerekir. Maddeyi ana maddeye formül satırı olarak iliştirebilirsiniz. Rota, alt yüklenicinin operasyon kaynağına tahsis edilen bir operasyon içermelidir. Bu operasyon, formül satırına, **İşlem No** alanı kullanılarak iliştirilir. alanda kullandığınızda otomatik olarak işaretlenir. |

## <a name="formula-versions"></a>Formül sürümleri
Yeni bir formül oluşturduğunuzda ve kendi belirli özelliklerini ve formül satırı maddelerini eklemeden önce ilk olarak bir formül sürümü oluşturmalısınız. Her formülün en az bir versiyonu olmalıdır. Bir formül sürümündeki **Onaylandı** düğmesi, yalnızca sürüm kaydı başarıyla kaydedildikten sonra kullanılabilir olur. Her bir formül sürümü kaydı, tamamlanmış ürünü ürettiğinizde üretilebilen bir veya daha fazla ortak ürün ve yan ürün ile ilişkilendirilir. Pek çok ürün, farklı toplu iş ebatlarında aynı içeriklerden üretilebilir; çoklu olarak veya farklı verimle. Bir formülün gerekli sayıda sürümünü oluşturabilirsiniz.

Birden fazla etkin formül versiyonunu yönetmek üzere yürürlük tarihi aralıkları veya "başlangıç" miktarı alanlarını kullanın. Birden fazla etkin formül versiyonu ancak tarih aralığı ve "başlangıç" miktarı çakışmıyorsa var olabilir.

Bir ürün reçetesinin çoğu zaman pek çok ürün reçetesi sürümüyle ilişkilendirilmiş olduğu ürün reçetelerinin aksine, genellikle yalnızca bir formül sürümü bir formül başına mevcuttur. Yalnızca bir formül sürümünün, belirli bir ürün için kapsama boyutları ve miktarı için etkinleştirilebileceğini unutmayın. Ancak, çok sayıda formül sürümü başka sebeplerle mevcut olabilir ve bir toplu iş emri oluşturduğunuzda bunları el ile seçebilirsiniz.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Formülleri ve formül sürümlerini onaylama ve etkinleştirme
Formüllerin ve formül versiyonlarının planlama ve üretim kullanılabilmeleri için önce onaylanması gerekir. Formüller kullanmadan önce genellikle etkinleştirilir. Bununla birlikte, üretim sırasında onaylanmış, ancak etkin olmayan bir formül sürümü seçebilirsiniz.

Bir formül veya formül sürümünü güvenlik altına almaya yardımcı olmak için **Düzenlemeyi engelle** veya **Onayın kaldırılmasını engelle** parametrelerini **Üretim denetim parametreleri** sayfasında ayarlayabilirsiniz.

**Düzenlemeyi engelle**'yi seçerseniz ve formül onaylanırsa, formül satırlarındaki hiçbir alan silinemez veya değiştirilemez. Bununla birlikte, formülün onayını kaldırırsanız, formül satırlarını silebilir ve değiştirebilirsiniz. Yeni formülleri ve yeni formül sürümleri oluşturabilirsiniz.

**Onayın kaldırılmasını engelle**'yi seçerseniz, onaylanmış bir formülün veya formül sürümünün onayını kaldıramazsınız. Ancak, yeni formüller ve yeni formül sürümleri oluşturabilirsiniz ve formül sürümünün etkinleştirmesini kaldırabilirsiniz.

Elektronik imza işlevini kullanarak birden çok düzeyde denetim ekleyebilirsiniz. Bir kullanıcı, formül onayı sırasında elektronik imza gerekecek şekilde ayarlanmışsa, bir **İmza** sayfası, formül etkinleştirildiğinde görüntülenir. Kullanıcı, elektronik imzalama yetkisine sahip olmalıdır ve değişiklik kabul edilmesi için sertifikanın başarılı şekilde doğrulanması gerekir. İmzanın kimlik doğrulaması yapılamazsa, onaylama veya onay kaldırma işlemi reddedilir ve onay veya onay kaldırmayı başlatan değişiklik başlangıçtaki durumuna geri döner.

## <a name="use-the-scalable-feature"></a>Ölçeklenebilir özelliği kullanmak
Ölçeklenebilir özellik, yalnızca formüldeki tüm madde bileşenleri **Değişken tüketim** olarak ayarlanmışsa kullanılabilir. Bu özellik, madde bileşenleri **Sabit tüketim** veya **Adım tüketimi** olarak ayarlanmışsa kullanılamaz. Ölçeklenebilir özellik kullanılırsa, bir formüldeki bir bileşende yaptığınız herhangi bir değişiklik, seçtiğiniz diğer bileşenlerin miktarlarını da değiştirir. Formül boyutu da ayarlanır. Benzer şekilde, formül boyutunu değiştirirseniz, tüm ölçeklenebilir içeriklerin miktarı değişir. Bu özellik, formül oluşturma ve bakımı içindir. Bir içeriğin miktarının toplu iş emrinde yukarı veya aşağı ölçeklendirilecek olup olmadığını belirtmez.

## <a name="use-step-consumption"></a>Adım tüketimi kullan
Adım tüketimi, bir içerik için **Formül satırı** sekmesinde miktar girme gereksinimini kaldırır. Bunun yerine, Adım tüketimi, bir **Başlangıç serisi** değeri ve **Miktar** değerine sahip olacak şekilde yapılandırılır. Toplu iş emri üzerindeki miktarı sağlayan Seri kaydı başına Adım tüketiminden gelen bilgi seçilir. Adım tüketimi, tüketim oranı toplu iş emri boyutuna göre doğrusal olmadığında faydalıdır ve gereksinimi yalnızca belirli bir miktar eşiği aşıldığında artırır. Bu özelliği yeni bir formül için etkinleştirmek için **Tüketim hesaplaması** grubu altında, uygulanabilir içerik için formül ayarını **Standart**'tan, **Adım**'a değiştirin. Bu tüketim yöntemini **Formül satırı** sayfasının **Kurulum** sekmesinde belirtirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]