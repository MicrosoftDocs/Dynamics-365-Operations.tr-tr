---
title: "Ürün bilgilerine genel bakış"
description: "Bu konu ürün bilgileri yönetimi hakkında bilgiler sağlar. Ürün bilgileri yönetimi paylaşılan ürün tanımı, kategori ve tüm tüzel kişilikler üzerindeki tanımlayıcıların yanı sıra iş süreçlerine uyum sağlamak üzere belirli ürün yapılandırmalarıyla birlikte çalışır."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 72dbc5d383352d4d6444d07495fdef00137b1c7f
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="product-information-overview"></a>Ürün bilgilerine genel bakış

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Bu konu ürün bilgileri yönetimi hakkında bilgiler sağlar. Ürün bilgileri yönetimi paylaşılan ürün tanımı, kategori ve tüm tüzel kişilikler üzerindeki tanımlayıcıların yanı sıra iş süreçlerine uyum sağlamak üzere belirli ürün yapılandırmalarıyla birlikte çalışır. 

Ürün bilgileri, tedarik zincirinin ve tüm sektörler arasındaki perakende uygulamalarının temelini oluşturur. Ürünler hakkındaki merkezi olarak yönetilen bilgilere (örneğin tedarik zincirlerinde) odaklanan süreçlere ve teknolojilere başvurur. Paylaşılan ürün tanımlarının, belgelerin, özniteliklerin ve tanımlayıcıların kullanılması önemlidir. Bir iş çözümünün çeşitli modüllerinde ürüne özgü bilgiler ve konfigürasyon, belirli ürünlerle ilgili iş süreçlerinin yönetilmesi için gereklidir.

## <a name="product-definition"></a>Ürün tanımı

Ürün birincil olarak bir ürün numarası, adı ve açıklamasıyla tanımlanır. Bununla birlikte, bir ürünü veya hizmeti açıklamak için başka veriler de gereklidir:

- Ürün türü: Madde veya hizmet
- Ürün alt türü: Farklı ürünler veya ana ürünler
- Ürün çeşidi modelinin tanımı:

     - Ürün boyutları ve boyut grupları
     - Ürün terminolojisi
     - Ürün konfigürasyon modelleri

- Ürünü bir veya daha fazla kategoriyle ilişkilendirme
- Ürün ve kategori öznitelikleri tanımı
- Ürün resimleri
- Ekler
- Ölçü birimleri ve ilgili dönüştürmeler
- Tüm adların ve açıklamaların çevirileri

## <a name="distribution-export-and-import-of-product-data"></a>Ürün verilerini dağıtma, dışa aktarma ve içe aktarma

Ürün tanımı Microsoft Dynamics 365 for Finance and Operations'da oluşturulabilir. Ayrıca ürün yaşam döngüsü yönetimi (PLM), ürün veri yönetimi (PDM) veya ürün bilgi yönetimi (PIM) sistemlerinden de alınabilir. Birden fazla Finance and Operations kurulumu kullanıldığında, bir kurulum diğer tüm kurulumlar için tipik olarak ürün verileri aslı olarak kullanılır. Bu yaklaşım, bir kurulumdan diğerine ürün tanımı bilgilerini aktarmaya olanak tanıyan geniş bir veri varlıkları kümesi tarafından desteklenir.

Ürün verilerinin birden çok kuruluma dağıtılmasını desteklemek amacıyla Finance and Operations Common Data Service kullanmanıza olanak tanır. Ürün tanımları bir Finance and Operations kurulumundan Common Data Service'a aktarılabilir. Ürün tanımları daha sonra ürün verileriyle Microsoft Dynamics 365 for Sales gibi diğer iş uygulamalarını sağlamak için kullanılabilir.

Dinamik ve çevik kuruluşlarda ürün bilgileri verilerinin her gün değiştiğini unutmayın. Bu nedenle, verilerin doğru ve gerçek ürün verilerinin korunması kendi başına önemli bir iş sürecidir.

## <a name="product-masters-and-product-variants"></a>Ana ürünler ve ürün çeşitleri

Ürünlerin müşteri gereksinimlerine hızlı şekilde uyarlandığı çevik bir dünyada, ürün tanımları farklı ürünler yerine ürün kümelerini belirtir. Microsoft Dynamics 365 for Finance and Operations'da bu genel ürünler *ana ürünler* olarak da bilinir. Ana ürünler, farklı ürünlerin iş süreçlerinde nasıl açıklanacağını ve davranacağını belirten tanımı ve kuralları tutar. Bu tanımlara bağlı olarak, farklı ürünler oluşturulabilir. Bu farklı ürünler *ürün çeşitleri* olarak da bilinir.

Finance and Operations'da, bir ana ürün ürün boyut grubu ve iş kurallarını belirtmek için bir konfigürasyon teknolojisi ile ilişkilidir. Ürün boyutları (Renk, Boyut, Stil ve Konfigürasyon) ilgili ürünlerin belirli davranışlarını tanımlamak ve izlemek için uygulama genelinde kullanılabilen belirli bir öznitelikler kümesidir. Bu boyutlar kullanıcıların ürünleri aramasına ve tanımlamasına da yardımcı olur.

## <a name="configuration-technologies"></a>Yapılandırma teknolojileri

Üç yapılandırma teknolojisi arasından seçim yapabilirsiniz:

- Önceden tanımlanan çeşitler önceden tanımlanmış ürün boyutlarıyla tanımlanır. Çeşit tanımı belirli bir geçerli boyut kombinasyonunu (örneğin Renk, Stil ve Boyut) içerir. Her kombinasyon farklı bir ürün çeşidi oluşturur.
- Boyut tabanlı yapılandırma genellikle üretim senaryolarında kullanılır ve ürün reçetelerinin (BOM) tanımında Yapılandırma boyutu kullanmanıza olanak tanır. Belirli bir yapılandırma seçildikten sonra sistem planlama ve üretim açısından bu yapılandırma için geçerli olan ürün reçetesi satırlarının alt kümesini kullanır. Bu kavram *genel ürün reçetesi* olarak da bilinir, çünkü bir ürünün tüm yapılandırmaları için paylaşılan bir ürün reçetesi kullanılır.
- Kısıtlama tabanlı yapılandırma, bir ürünün tüm olası çeşitlerini tek bir modelde açıklamak için gerekli olan tüm olası öznitelikleri ve bileşenleri açıklamak üzere bir ütün yapılandırma modeli kullanır. Öznitelik kombinasyonlarının kısıtlamaları, normal ifadelerle veya tablo tabanlı kısıtlamalarla açıklanabilir. Yapılandırma modelleri ve yapılandırıcılar ürün bilgileri yönetiminde daha önemli hale gelir ve tüm sektörler üzerinde kullanılır.

Finance and Operations uygulamasını planlarken, iş süreci için doğru yapılandırma teknolojisini seçmeniz çok önemlidir. Bir ürün uygulamadan sonra bir modelden başka bir modele dönüştürülemez.

## <a name="product-variant-model-definition-workspace"></a>Ürün çeşidi model tanımı çalışma alanı

**Ürün çeşidi model tanımı** çalışma alanı ana ürünler hakkında genel bilgi verir. Ayrıca, belirli tüzel kişilikler için ana ürün ve ilgili ürün çeşitlerinin serbest bırakılma durumunu da gösterir.

## <a name="released-products"></a>Serbest bırakılan ürünler

Belirli bir tüzel kişilik için serbest bırakılan ürünler *serbest bırakılan ürünler* olarak bilinir. Ürünler toplu halde tek bir tüzel kişiliğe veya bir kerede birçok tüzel kişiliğe serbest bırakılabilir. Tüzel kişilik başına eklenecek çeşitli ürün özellikleri ve öznitelikleri olabileceğinden, **Serbest bırakılan ürün bakımı** çalışma alanı, her tüzel kişilikte veya tüzel kişiliğin alt kuruluşunda yakın zamanda serbest bırakılan ürünleri izleme ve tamamlama olanağı sağlar.

### <a name="released-product-maintenance-workspace"></a>Serbest bırakılan ürün bakımı çalışma alanı

**Serbest bırakılan ürün bakımı** çalışma alanını **Çalışma alanımı yapılandır** menü öğesinden yapılandırabilirsiniz. Çalışma alanını filtrelemek için kullanılacak bir kategori hiyerarşisi ve kategori seçin. Çalışma alanında ilgili ürün verilerini ayarlamak üzere **Yakın zamanda serbest bırakılan ürünler** ve **Durdurulan serbest bırakılmış ürünler** için zaman dilimlerini gün cinsinden de tanımlayabilirsiniz.

Çalışma alanı kutucukları özetinden ve iki listeden oluşur. **Açık servis talepleri** listesi, seçilen ürün kategorisi hiyerarşisinde tamamlanmamış ve kapatılmamış ürünleri bulunan ürün değişikliği durumlarını gösterir. **Yakın zamanda serbest bırakılan** listesi çalışma alanı yapılandırmasında ayarlanan zaman dilimi içinde serbest bırakılmış olan ürünleri gösterir. Listedeki her madde için doğrulama çalıştırılır ve doğrulama durumu gösterilir. Bu durum tüzel kişilik için gerekli yapılandırmaların tamamlanmamış olduğunu gösterebilir. Ürünün gerekli yapılandırmasını tamamlamak için listeden **Serbest bırakılan ürün ayrıntıları**, **Ürün özniteliği bakımı**, **Ürün kategorisi bakımı**, **Varsayılan sipariş ayarları** ve **Metin çevirileri** sayfalarına doğrudan erişebilirsiniz.

### <a name="manually-creating-a-new-released-product"></a>Yeni serbest bırakılan ürünü el ile oluşturma

Kuruluşun iş süreçlerine ve bu işlevin kullanılıp kullanılmayacağıyla ilgili kurallara bağlı olarak tek bir çalıştırmada el ile serbest bırakılan ürün oluşturabilirsiniz. Bu işlev yeni bir ürün oluşturur ve bunu otomatik olarak geçerli tüzel kişiliğe serbest bırakır. Yeni ürün oluşturmak için **Serbest bırakılan ürün bakımı** çalışma alanında veya **Serbest bırakılan ürün** liste sayfasında **Serbest bırakılan ürünler**'e tıklayın.

