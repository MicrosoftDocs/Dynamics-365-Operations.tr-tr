---
title: Stok yenileme
description: "Bu makalede Ambar yönetiminde bulunan işlevi kullanan ambarlarda kullanılabilen stok yenileme stratejileri açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c808ec202bdb271f08a36a2b25ebed22a9477414
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="replenishment"></a>Stok yenileme

[!include[banner](../includes/banner.md)]


Bu makalede Ambar yönetiminde bulunan işlevi kullanan ambarlarda kullanılabilen stok yenileme stratejileri açıklanmaktadır.

Bu makalede Ambar yönetiminde bulunan işlevi kullanan ambarlarda kullanılabilen stok yenileme stratejileri açıklanmaktadır. Bu bilgiler Stok yönetiminde bulunan ambar çözümü için geçerli değildir. Kullanılabilen üç stok yenileme stratejisi bulunmaktadır:

-   **Dalga talep stok yenilemesi** – Bu strateji dalga işi oluşturduğunda stok kullanılamıyorsa giden siparişler veya yükler için stok yenileme işi oluşturur. Örneğin stok yenileme işi bir satış siparişi için gerekli olan miktar dalga işlendiğinde kullanılabilir durumda olmadığında oluşturulabilir.
-   **Min/Maks stok yenileme** – Bu strateji yerleşimlerde stok yenilemesi yapılması gereken zamanları belirlemek için minimum ve maksimum stoklama sınırları kullanır. Madde ve yerleşim ölçütleri stok yenileme için değerlendirilen stoğu belirler. Min/Maks stok yenileme şablonları malzeme çekme yerleşimlerinde optimum düzeyleri korumak için kullanılan birincil mekanizmadır. Dalga talebi karşılamak için yeterli malzeme çekme stoğunun garantilenmesine yardımcı olmak için Min/Maks stok yenileme döngüleri arasında bir ek olarak talep stok yenileme özelliğini kullanabilirsiniz.
-   **Yük talebi stok yenilemesi** – Bu strateji birkaç yüke ait talebi toplar ve ilgili malzeme çekme yerleşimlerinde stok sağlamak için gerekli stok yenileme işini oluşturur. Bu strateji oluşturulan yüklerin serbest bırakıldıktan sonra ambardan çekilebilmesini garantilemeye yardımcı olur.

Bu üç strateji stok yenileme şablonuna dayalı olarak stok yenileme işi oluşturur.

## <a name="wave-demand-replenishment"></a>Dalga talebi stok yenilemesi
Giden siparişler veya yükler için gereken miktar dalga işi oluşturduğunda kullanılamıyorsa dalga talebi stok yenilemesi talebe göre stok yenileme işi oluşturur. Stok yenileme şablonu madde ölçütleri, ölçü birimi, talep artışı ve yerleşim hakkında bilgiler içerir. 

Yerleşim yönergeleri stok yenilemesi yapılması gereken yerleşimi belirlemek için kullanılır. Bu yerleşim yönergelerini stok yenileme şablonuna **Yönerge kodu** alanını kullanarak bağlayabilirsiniz. **Yönerge kodu** alanı ayarlanmamışsa, kullanılması gereken yerleşim yönergesini belirlemek için sorgular kullanılır. Stok yenileme şablonunda bir yönerge kodu belirtilmemişse ve yerleşim yönergesinin bir yönerge kodu varsa, yerleşim yönergesindeki sorgu doğru olsa bile yerleşim yönergesi yoksayılır. Malzeme çekme yerleşimi yönergeleri stok yenilemesi için stok alınması gereken konumu belirlemek için kullanılır. 

Şablon oluşturmaya ek olarak, dalga şablonunda da bazı stok yenileme ayarlarını belirtmeniz gerekir. Dalga şablonu yalnızca bir maddenin dağıtımı başarılı olmadığında çalıştırılan stok yenilemesi için bir dalga adımı içermelidir. Bu stok yenileme dalga adımı kullanılması gereken stok yenileme şablonunu belirlemek için bir dalga adımı kodu kullanır. Stok yenileme için bir dalga adımı oluşturmaya ek olarak, dalga şablonunun **Yöntemler** bölümünde **stok yenileme** öğesinin seçildiğinden emin olmanız gerekir. 

**Stok yenileme şablonu** sayfasında **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver** onay kutusu bulunmaktadır. Seçili stok yenileme şablonundan oluşturulan işten rezerve edilmemiş miktarları düşmek için talep stok yenilemesine izin vermek istiyorsanız bu onay kutusunu işaretlemeniz gerekir. Talep stok yenilemesi şablonlarını bu mantığı kullanmak üzere etkinleştirmek üzere, mevcut tüm stok yenileme şablonları için bu onay kutusunu ayarlamanız gerekir. İş, **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver** onay kutusunun seçili olduğu stok yenileme şablonlarında oluşturulmuşsa, ambarda talep stok yenilemesi tetiklendiğinde, rezerve edilmemiş miktara sahip mevcut stok yenileme işinden bu talep düşürülür.

## <a name="minmax-replenishment"></a>Min/Maks stok yenileme
Min/Maks stok yenilemede stok ayarlanmış minimum ve maksimum sınırlar arasında yenilenir. Genellikle malzeme çekme işlemi başlamadan önce tüm malzeme çekme yerleşimlerinin maksimum düzeyde dolu olmasını sağlamaya yardımcı olmak üzere bu işlem her gün bir kere gerçekleştirilir. 

Minimum ve maksimum tutarlar stok yenileme şablonunda ayarlanır. Şablondaki diğer ayarların çoğu dalga talebi stok yenilemesinde kullanılan şablonlardaki ayarlara benzer. Şablonda her madde ve yerleşim için bir satır olmalıdır. Stok yenilemeyi toplu iş kullanarak çalıştırdığınızda Microsoft Dynamics 365 for Operations satırların düzenlendiği sırayla, stok yenilemenin gerekli olup olmadığını değerlendirir. 

Min/Maks stok yenileme stratejisinin madde için sabit yerleşim olarak ayarlanmamış boş yerleşimlerde stok yenilemesi yapamayacağını unutmayın. Stok yenilemesi yapılması gereken yerleşim sabit bir yerleşim değilse, Dynamics 365 for Operations stok yenilemesi yapılacak maddeyi belirleyemez. Bu nedenle stok yenileme işlemi gerçekleşmeden önce eldeki miktarın en az bir kısmı gereklidir.

## <a name="load-demand-replenishment"></a>Yük talebi stok yenilemesi
Yük talebi stok birkaç yüke ait talebi toplar ve ilgili malzeme çekme yerleşimlerinde stok sağlamak için gerekli stok yenileme işini oluşturur. Yük talebi stok yenilemesi pek çok açıdan Dalga talep stok yenilemesine benzer. Aralarındaki temel fark Yük talebi stok yenilemesi ve Dalga talep stok yenilemesinin çalıştırıldığı durumlardır. Min/Maks stok yenileme gibi yük talebi stok yenilemesi toplu işlem kullanılarak çalıştırılır. Toplu iş ayarlamak için **Yük talebi stok yenilemesi** sayfasında, kullanılacak stok yenileme şablonunu seçin ve talebi belirlemek için kullanılacak yükleri belirten bir filtre sorgusu ayarlayın. Yerleşim sorgusu yüklerin toplam talebini karşılamak için kullanılabilir miktarın çıkarılacağı yerleşimleri belirler.

## <a name="replenishment-prerequisites"></a>Stok yenileme önkoşulları
| Önkoşul            | Açıklama                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Madde                    | Madde mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.                                                                                                                                                                                       |
| Ambar               | Ambar mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir. Ambarı ambar yönetim süreçleri için etkinleştirmek üzere, **Ambarlar** sayfasında ambarı seçin, ardından **Ambar yönetim süreçlerini kullan** seçeneğini belirleyin. |
| Stok yenileme şablonları | Min/Maks stok yenileme, Dalga talep stok yenilemesi veya Yük talebi stok yenilemesi için en az bir stok yenileme şablonu ayarlanmalıdır.                                                                                                             |
| Konumlar               | Yerleşimler oluşturulmalı ve bir yerleşim profiline bağlanmalıdır.                                                                                                                                                                                     |
| Konum profilleri       | Yerleşim profilleri yerleşimleri oluşturmak için gereklidir.                                                                                                                                                                                       |
| Konum yönergeleri     | Yerleşim yönergeleri işi stok yenilemenin gerektiği yerleşimlere ve stok kaynağı olarak kullanılacak yerleşimlere yönlendirmek için gereklidir.                                                                                     |
| İş şablonları          | **Stok yenileme** türünün iş şablonları stoğu istenen yerleşimlere taşıyabilmek üzere stok yenileme işi oluşturmak için gereklidir.                                                                                           |





