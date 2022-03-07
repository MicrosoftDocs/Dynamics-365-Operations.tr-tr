---
title: Mühendislik değişim yönetimi için ortak değerler oluşturma
description: Bu konu, mühendislik değişikliği yönetiminin çeşitli bölümlerindeki parametreler için kullanılan ortak değerlerin nasıl kurulacağını açıklar.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65f86fc488fe25cd4b093461088134fd7ad0c45ca569cd8f751314f1f5d88b6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753312"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Mühendislik değişim yönetimi için ortak değerler oluşturma

[!include [banner](../includes/banner.md)]

Mühendislik değişikliği yönetimini ayarladığınızda, kullanıcı arabiriminin (UI) diğer bölümlerindeki açılan listeleri doldurmak için kullanılacak birkaç değer topluluğu oluşturmanız gerekir. Bu değerleri, üretmeniz gereken ürün türlerine ve belirli iş gereksinimlerinize göre belirtmelisiniz.

## <a name="engineering-change-categories"></a>Mühendislik değişiklik kategorileri

Mühendislik değişikliği emirlerini yönetimi ve gözden geçirmesi daha kolay olacak şekilde düzenlemek için mühendisliği değişikliği kategorilerini kullanırsınız. Örneğin, belirli bir departmanın önerilen değişiklikleri gözden geçirmesi gerektiğinde kategoriye göre, iş akışı ayarlamayı yararlı bulabilirsiniz. Bu nedenle, mühendislik değişikliği emrinde bir **Kategori** alanı bulunur.

Şirketinizde kullanılan mühendislik değişikliği kategorileri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Mühendisliği değişikliği kategorileri**'ne gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="engineering-change-priorities"></a>Mühendislik değişiklik öncelikleri

Mühendislik değişikliği öncelikleri, mühendislik değişikliği emrinin önemini veya aciliyetini belirtmek için kullanılır. Bunlar, ilk olarak hangi emirlerin işlenmesi gerektiğini ve ne kadar hızlı bir şekilde işlem yapılacağını kolayca belirleyebilmenizi sağlayacak şekilde, bir mühendislik değişikliği emrinin önemini izlemenize yardımcı olabilirler.

Şirketinizde kullanılan mühendislik değişikliği öncelikleri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Mühendisliği değişikliği öncelikleri**'ne gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="engineering-change-reasons"></a>Mühendislik değişiklik nedenleri

Mühendislik değişikliği nedenleri, değişiklik emrinde değişikliğin nedenini veya yapısını belirtir.

Şirketinizde kullanılan mühendislik değişikliği nedenleri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Mühendisliği değişikliği nedenleri**'ne gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="material-disposal-codes"></a>Malzeme elden çıkarma kodları

Çöp alanınıza eklenmeden önce; bitmiş mallarda kullanılan malzemeleri veya belirli bir şekilde elden çıkarılmaları gereken bileşenleri sınıflandırmak veya bir işlem gerektirmek için malzeme elden çıkarma kodlarını kullanırsınız. Bir mühendislik değişikliği emrine ilgili ürün eklediğinizde, değişiklik ayrıntılarının parçası olarak bir elden çıkarma kodu atayabilirsiniz.

Şirketinizde kullanılan malzeme elden çıkarma kodları koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Malzeme elden çıkarma kodları**'na gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="received-customer-approval"></a>Alınan müşteri onayı

Belirli bir müşteri için ürünler tasarladığınızda, ürün hazır olarak ayarlanmadan önce tasarım ve özellikler çoğu zaman doğrulanmalıdır. **Müşteri onayı alındı** alanı, ürünün onay sürecinin hangi aşamasında olduğunu ve/veya onayın alınıp alınmadığını belirtmenize olanak tanır.

Şirketinizde kullanılan alınan müşteri onayı değerleri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Alınan müşteri onayı değerleri**'na gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Mühendislik değişikliği: Çevre sağlığı ve güvenlik kodları

Ürünün üretiminde standart çevre sağlığı veya güvenlik düzenlemelerinin veya şirkete özel düzenlemelerin veya yordamların dikkate alınmaları gerekiyorsa, bunları tanımlamak için çevre sağlığı ve güvenlik kodlarını kullanabilirsiniz. Mühendislik değişikliği emrinde, etkilenen ürünün ayrıntılarını düzenlerken ürünün üretim emri için geçerli olan kodları belirtebilirsiniz.

Şirketinizde kullanılan sağlık ve güvenlik değerleri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Çevre sağlığı ve güvenlik kodları**'na gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

## <a name="engineering-change-severities"></a>Mühendislik değişiklik önem dereceleri

Mühendislik değişikliği önem derecelerini, bir mühendislik değişikliği emrinde ürünler için geçerli olan etki düzeyini belirtmek için kullanırsınız.

Şirketinizde kullanılan mühendislik değişikliği önem dereceleri koleksiyonunu oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Mühendisliği değişikliği önem dereceleri**'ne gidin. Sonra değerleri eklemek, kaldırmak ve düzenlemek ve onları gösterildikleri açılan listelerde göründükleri düzende düzenlemek için Eylem bölmesindeki düğmeleri kullanabilirsiniz.

Oluşturduğunuz her önem düzeyi için geçerli olan kurallar oluşturabilirsiniz. Bu kuralların nasıl atanacağı hakkında daha fazla bilgi için sonraki bölüme bakın.

## <a name="engineering-change-severity-rule-sets"></a>Mühendislik değişiklik önem derecesi kural kümeleri

Etkilenen ürünlerde yapılan değişikliklerin türüne göre değişiklik sırasının önemini otomatik olarak hesaplamak için kullanabileceğiniz bir grup kural oluşturmak için mühendislik değişikliği önem derecesi kural kümeleri kullanılır. Önem derecesi kurallarını kullanmak için **Mühendislik değişikliği yönetimi parametreleri** sayfasını açın ve **Önem derecesi kuralı** alanını *Hesapla* veya *Otomatik olarak hesapla* şeklinde ayarlayın.

Sistem önem derecesini değerlendirirken, kuralları sayfada göründükleri sırada, yukarıdan aşağıya doğru işler. Bir kuralın seçilmesini ve önceliğinin ayarlanmasını sağlamak için bir kural kümesindeki tüm kuralların karşılanması gerekir.

Tanımladığınız her bir değişiklik önem düzeyi için geçerli olan kuralları ayarlamak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi \> Mühendislik değişikliği önem derecesi kural kümeleri**'ne gidin. Ardından şu adımlardan birini izleyin.

- Yeni kural kümesi oluşturmak için, Eylem bölmesinden **Yeni**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Mevcut kural kümesini düzenlemek için,liste bölmesinden durumu seçin ve Eylem bölmesinden **Düzenle**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Var olan bir kural kümesini silmek için bunu liste bölmesinden seçin ve sonra Eylem bölmesinden **Sil**'i seçin.
- Kural kümelerinin listesini yeniden düzenlemek için liste bölmesinde bir kural kümesi seçin ve sonra yeniden konumlandırmak için Eylem bölmesindeki **Yukarı** ve **Aşağı** düğmelerini kullanın.

Her kural kümesinde, aşağıdaki alanı ayarlayın:

- **Önem derecesi**: Kuralın oluşturulacağı önem düzeyini seçin. Düzeyler oluşturmak ve adlandırmak için **Mühendislik değişikliği önem dereceleri** sayfasını kullanırsınız. (Daha fazla bilgi için önceki bölüme bakın.)

Geçerli önem derecesi ayarına kural eklemek veya var olan bir kuralı kaldırmak için **Kurallar** hızlı sekmesindeki düğmeleri kullanın. Her kuralda bir **Kural** alanı ve bir **Ad** alanı vardır. Kurallar sistem tarafından kurulur ve bir ürünün sahip olabileceği değişiklik türlerini gösterir. Ad, değişiklik türünü gösterir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]