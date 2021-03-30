---
title: Ürün çeşidi yönetimi
description: Bu konu Dynamics 365 Commerce'da ürün çeşidi yönetiminin temel kavramlarını açıklar ve projeniz için uygulamayla ilgili önemli notlar sağlar.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 6a7a488b6684c23ceac9f35abf9e93e5c7261eb9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211510"
---
# <a name="assortment-management"></a>Ürün çeşidi yönetimi

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Genel bakış

Dynamics 365 Commerce, kanallar arasında ürün kullanılabilirliğini yönetmenizi sağlayan *ürün çeşitleri* sunar. Ürün çeşitleri, belirli mağazalarda ve belirli bir dönemde hangi ürünlerin kullanılabilir olduğunu belirler.

Commerce'de, ürün çeşidi bir veya daha fazla kanalın (veya kuruluş hiyerarşileri kullanıldığında kanal grupları) bir veya daha fazla ürünle (kategori hiyerarşileri kullanıldığında ürün grupları) eşlenmesidir.

Bir kanalın genel ürün karışımı kanala atanan yayımlanmış ürün çeşitleri tarafından belirlenir. Bu nedenle, her kanal için birden fazla etkin ürün çeşidi yapılandırabilirsiniz.

### <a name="basic-assortment-setup"></a>Temel ürün çeşidi kurulumu

Aşağıdaki örnekte, her mağaza için benzersiz bir sınıflama yapılandırılmıştır. Bu durumda, ürün 1 mağaza 1'de kullanılabilir ve yalnızca ürün 2 mağaza 2'de kullanılabilir.

![Her ürün bir mağazada kullanılabilir](./media/Managing-assortments-figure1.png)

Ürün 2'yi mağaza 1'de kullanılabilir yapmak için, ürünü ürün çeşidi 1'e ekleyebilirsiniz.

![Ürün 2 ürün çeşidi 1'e eklenir](./media/Managing-assortments-figure2.png)

Alternatif olarak, mağaza 1'i ürün çeşidi 2'ye ekleyebilirsiniz.

![Mağaza 1 ürün çeşidi 2'ye eklenir](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Kuruluş hiyerarşileri

Aynı ürün çeşitlerini paylaşan birden fazla kanal olması durumunda, ürün çeşitlerini Commerce ürün çeşidi kuruluş hiyerarşisini kullanarak yapılandırabilirsiniz. Bir hiyerarşiden düğümler eklendiğinde, bu düğümdeki tüm kanallar ve alt düğümleri dahil edilir.

![Kuruluş hiyerarşisi](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Ürün kategorileri

Benzer şekilde, ürün tarafında, ürün kategorisi hiyerarşilerini kullanarak ürün grupları ekleyebilirsiniz. Bir veya daha fazla kategori hiyerarşisi düğümü ekleyerek ürün çeşitlerini yapılandırabilirsiniz. Bu durumda, ürün çeşidi bu kategori düğümündeki ve onun alt düğümlerindeki tüm ürünleri içerir.

![Ürün kategorileri](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Dışarıda bırakılan ürünler veya kategoriler

Ürün çeşitlerine ürünler ve kategoriler eklemeye ek olarak, ürün çeşitleri dışında tutulması gereken belirli ürünleri veya kategorileri tanımlamak için Dışarıda tut seçeneğini kullanabilirsiniz. Aşağıdaki örnekte, belirli bir kategorideki ürün 2 dışındaki tüm ürünlerin eklenmesi isteniyor. Bu durumda, ürün çeşidini tek tek ürünler olarak tanımlamanız veya ek kategori düğümleri oluşturmanız gerekmez. Bunun yerine, yalnızca kategoriyi dahil edip ürünü dışarıda tutabilirsiniz.

> [!NOTE]
> Bir ürün tanımına göre bir veya daha fazla ürün çeşidine hem dahil ediliyor hem de dışarıda bırakılıyorsa, ürün daima dışarıda bırakılmış olarak kabul edilir.

![Hariç tutulan ürün](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Genel ve serbest bırakılan ürünler

Ürün çeşitleri genel düzeyde tanımlanır ve birden fazla tüzel kişiliğe ait kanallar içerebilir. Ürün çeşitlerine dahil edilen ürünler ve kategoriler tüzel kişilikler arasında paylaşılır. Ancak, bir ürünün gerçekte satılabilmesi, sipariş edilebilmesi, sayılabilmesi veya kanalda alınabilmesi için serbest bırakılması gerekir (örneğin, satış noktasında\[POS\]). Bu nedenle, farklı tüzel kişiliklerdeki iki mağaza aynı ürünleri içeren bir ürün çeşidini paylaşabilmesine karşın ürünler yalnızca bu tüzel kişiliklere serbest bırakılmış olması durumunda kullanılabilir.

### <a name="dynamic-and-static-assortments"></a>Dinamik ve statik ürün çeşitleri

Ürün çeşitleri belirli kanallar ve ürünlerle veya kuruluş birimleri ve kategorileri dahil edilerek tanımlanabilir. Bu gruplara referanslar içeren ürün çeşitleri dinamik ürün çeşitleri olarak kabul edilir. Bu grupların tanımı veya içerikleri ürün çeşidi etkinken değişirse, ürün çeşidi tanımı da değişir.

Örneğin, bir ürün çeşidi başlangıçta tanımlanmış ve yayımlanmış olup bir ürün kategorisine referans vermektedir. Kategoriye daha sonra ek ürünler eklenmesi durumunda, bu ürünler otomatik olarak mevcut ürün çeşidinin tanımına dahil edilir. Ürünlerini ürün çeşidine el ile eklemeniz gerekmez. Benzer şekilde, bir kuruluş birimi farklı bir düğüme eklenirse, kuruluş biriminin ürün çeşidi otomatik olarak bu tanıma göre ayarlanır.

### <a name="stopped-products"></a>Durdurulan ürünler

**Varsayılan sipariş** ayarlarındaki bir ayarı açarak serbest bırakılan ürünleri satış işlemi için durdurabilirsiniz. Bu ayar çoğunlukla bir ürün ömrünün sonuna geldiğinde ve herhangi bir kanalda satılmaması gerektiğinde kullanılır. Ürün çeşitleri bu ayarı dikkate alır ve durdurulan ürünler, ürün çeşidi yapılandırmasına bakılmaksızın ürün çeşidi içinde sınıflandırılmaz.

### <a name="blocked-products"></a>Engellenen ürünler

Bir ürünün satışını durdurmanın yanı sıra, bir ürünün satışını geçici olarak bloke edebilirsiniz. Bu ayarı serbest bırakılan bir ürünün **Commerce** sekmesinde yapılandırabilirsiniz. Engellenen ürünler ürün çeşidi içinde sınıflandırılmaya devam eder ancak POS'ta ürünün satılamayacağını bildiren bir ileti alırsınız.

### <a name="date-effectivity"></a>Tarih etkililiği

Ürün çeşitlerinin geçerlilik tarihi vardır. Bu nedenle, perakendeciler ürünlerin kanalda ne zaman kullanılabileceğini veya kullanılamayacağını yapılandırabilir. Ürün çeşitlerini önceden tanımlayıp yayımlayabilir ve başlangıç ve bitiş tarihlerini belirtebilirsiniz. Ürünler otomatik olarak belirtilen tarihlerde kullanılabilir veya kullanılamaz olur.

### <a name="process-assortments-batch-job"></a>Ürün çeşidi toplu işi yürütme

Commerce'de tanımlanan ürün çeşitlerinin geçerli olabilmesi için önce işlenmesi gerekir. Bu işlem aşağıdaki nedenlerle yapılır:

- Kanalların daha kolay kullanabilmesi için ürün çeşitleri tanımlarının normal dışı hale getirilmesi gerekir. Bir kanal için bir ürün yelpazesi, çeşitli tarih aralıklarına yayılan birden fazla ürün çeşidiyle tanımlanabilir. Bu bilgilerin bazıları önceden sunucu üzerinde hesaplandığında, kanal performansı artar.
- Ürün çeşidindeki ürünler ve kategoriler ürün çeşidinin dışında değişebilir. Kategorilere veya kuruluş birimlerine referanslar içeren dinamik ürün çeşitlerinin dönemsel olarak işlenmesi gerekir; böylece ürün çeşitleri geçerli atamalarına bağlı olarak kayıtları içeride veya dışarıda tutabilir.

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar

Commerce uygulamanız için ürün çeşitlerini planlayıp yönetirken aşağıdaki uygulama gereksinimlerini göz önünde bulundurun:

- **Veri yineleme ve veritabanı boyutu** – Ürün çeşitleri ürün kullanılabilirliğini yönetmek açısından işletmenin ihtiyacını karşılamanın yanı sıra kanalın boyutunu ve çevrim dışı veritabanlarını yönetmek için de önemli bir araçtır. İyi yönetilen ürün çeşitleri işlenmesi ve kanala ve çevrimdışı veritabanına kopyalanması gereken veri miktarını azaltmaya yardımcı olur. Ayrıca, kalıcı olması gereken kayıt sayısını da azaltmaya yardımcı olur. Bu veritabanlarında daha az sayıda kayıt bulunması bir harekete, aramaya maddeler eklediğinizde ve ürünlere göz attığınızda performansı artırır.
- **Geçerlilik tarihi/sona eren ürün çeşitleri** – Kanaldaki ve çevrimdışı veritabanlarındaki ürünlerin sayısını yönetmede kullanılan en etkili araçlardan biri ürün çeşitlerinin geçerlilik tarihi bulunmasıdır. Dönemsel ürünler veya ömrünün sonuna gelen ürünler için süreyi açık uçlu bırakırsanız (süresi sona ermeyen) bu veritabanları önemli derecede büyür. Bu durumu yönetmek için çeşitli yaklaşımlar kullanabilirsiniz. Örneğin, dönemsel ürünler ve her zaman kullanılabilir olan ürünler için ayrı ürün çeşitleri sağlayabilirsiniz.
- **Ürün çeşitleri dışındaki satışlar ve iadeler** – Bu özellik perakendecilerin kendi ürün çeşitlerini mağaza için temel ürün yelpazesine ait ürünler için ürün sayısını vererek etkin biçimde yönetmesine yardımcı olur. Bu özellik ayrıca perakendecilerin bir ürünün yanlışlıkla bir ürün çeşidinde eksik kalması ya da bir ürünün ürün çeşidine ilişkin geçerlilik tarihleri dışında iade edilmesi durumunda yardımcı olur.

Ürün verileri kanal veritabanında yoksa, POS gerekli bilgileri almak için merkeze gerçek zamanlı bir ağrı yapar ve böylece ürün satılabilir, iade edilebilir veya müşteri siparişine konulabilir. Bu şekilde alınan ürün bilgileri yalnızca bu hareket kapsamı süresince kullanılabilir. Ürün ürün çeşidi tanımına eklenmez. Bu nedenle, daha sonra gerektiğinde gerçek zamanlı çağrılar yapılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]