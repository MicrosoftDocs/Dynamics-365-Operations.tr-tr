---
title: Stok yenilemeye genel bakış
description: Bu konuda Ambar yönetiminde bulunan işlevi kullanan ambarlarda kullanılabilen stok yenileme stratejileri açıklanmaktadır.
author: Mirzaab
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d554a6d415ca3e720c71387e218e50215c288991
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996085"
---
# <a name="replenishment-overview"></a>Stok yenilemeye genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda Ambar yönetiminde bulunan işlevi kullanan ambarlarda kullanılabilen stok yenileme stratejileri açıklanmaktadır. Bu konudaki bilgiler Stok yönetiminde bulunan ambar çözümü için geçerli değildir.

Aşağıdaki stok yenileme stratejileri bulunmaktadır:

- **Dalga talep stok yenilemesi** – Bu strateji dalga işi oluşturduğunda stok kullanılamıyorsa giden siparişler veya yükler için stok yenileme işi oluşturur. Örneğin stok yenileme işi bir satış siparişi için gerekli olan miktar dalga işlendiğinde kullanılabilir durumda olmadığında oluşturulabilir.
- **Min/Maks stok yenileme** – Bu strateji yerleşimlerde stok yenilemesi yapılması gereken zamanları belirlemek için minimum ve maksimum stoklama sınırları kullanır. Madde ve yerleşim ölçütleri stok yenileme için değerlendirilen stoğu belirler. Min/Maks stok yenileme şablonları malzeme çekme yerleşimlerinde optimum düzeyleri korumak için kullanılan birincil mekanizmadır. Dalga talebi karşılamak için yeterli malzeme çekme stoğunun garantilenmesine yardımcı olmak için Min/Maks stok yenileme döngüleri arasında bir ek olarak talep stok yenileme özelliğini kullanabilirsiniz.
- **Yük talebi stok yenilemesi** – Bu strateji birkaç yüke ait talebi toplar ve ilgili malzeme çekme yerleşimlerinde stok sağlamak için gerekli stok yenileme işini oluşturur. Bu strateji oluşturulan yüklerin serbest bırakıldıktan sonra ambardan çekilebilmesini garantilemeye yardımcı olur.
- **Anında stok yenileme** – Bu strateji bir dalga çalışmadan önce, bir stok yenileme şablonuna sahip bir yerleşim yönergesi satırı için bir tahsisat başarısız olursa bir stoku yeniler. 

Bu dört strateji stok yenileme şablonuna dayalı olarak stok yenileme işi oluşturur.

## <a name="wave-demand-replenishment"></a>Dalga talebi stok yenilemesi
Üretim emirleri, kanbanlar, giden siparişler veya yükler için gereken miktar dalga işi oluşturduğunda kullanılamıyorsa dalga talebi stok yenilemesi talebe göre stok yenileme işi oluşturur. Stok yenileme şablonu madde ölçütleri, ölçü birimi, talep artışı ve yerleşim hakkında bilgiler içerir. 

Yerleşim yönergeleri stok yenilemesi yapılması gereken yerleşimi belirlemek için kullanılır. Bu yerleşim yönergelerini stok yenileme şablonuna **Yönerge kodu** alanını kullanarak bağlayabilirsiniz. **Yönerge kodu** alanı ayarlanmamışsa, kullanılması gereken yerleşim yönergesini belirlemek için sorgular kullanılır. Stok yenileme şablonunda bir yönerge kodu belirtilmemişse ve yerleşim yönergesinin bir yönerge kodu varsa, yerleşim yönergesindeki sorgu doğru olsa bile yerleşim yönergesi yoksayılır. Malzeme çekme yerleşimi yönergeleri stok yenilemesi için stok alınması gereken konumu belirlemek için kullanılır. 

Şablon oluşturmaya ek olarak, dalga şablonunda da bazı stok yenileme ayarlarını belirtmeniz gerekir. Dalga şablonu yalnızca bir madde başarıyla dağıtılmadığında çalıştırılan stok yenilemesi için bir dalga adımı içermelidir. Bu stok yenileme dalga adımı kullanılması gereken stok yenileme şablonunu belirlemek için bir dalga adımı kodu kullanır. Stok yenileme için bir dalga adımı oluşturmaya ek olarak, dalga şablonunun **Yöntemler** bölümünde **Stok Yenileme** öğesinin seçildiğinden emin olmanız gerekir. 

**Stok yenileme şablonu** sayfasında **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver** onay kutusu bulunmaktadır. Seçili stok yenileme şablonundan oluşturulan işten rezerve edilmemiş miktarları düşmek için talep stok yenilenecekse bu onay kutusunu işaretleyin. Talep stok yenilemesi şablonlarını bu mantığı kullanmak üzere etkinleştirmek üzere, mevcut tüm stok yenileme şablonları için bu onay kutusunu ayarlayın. İş, **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver** onay kutusunun seçili olduğu stok yenileme şablonlarında oluşturulmuşsa, ambarda talep stok yenilemesi tetiklendiğinde, rezerve edilmemiş miktara sahip mevcut stok yenileme işinden bu talep düşürülür.

**Stok yenileme birimi** stok yenilemesi yapılacak minimum birimdir. Bunun, birimin katı olan bir tamsayı olması gerekiyor. Sistem, iş oluşturulurken mümkün olan en yüksek birime kadar yuvarlayacak.

Talep stok yenilemesi satış siparişleri, transfer emirleri, üretim emirleri ve kanbanlar için desteklenir. 

## <a name="minmax-replenishment"></a>Min/Maks stok yenileme
Min/Maks stok yenilemede stok ayarlanmış minimum ve maksimum sınırlar arasında yenilenir. Genellikle malzeme çekme işlemi başlamadan önce tüm malzeme çekme yerleşimlerinin maksimum düzeyde dolu olmasını sağlamaya yardımcı olmak üzere bu işlem her gün bir kere gerçekleştirilir. 

Minimum ve maksimum tutarlar stok yenileme şablonunda ayarlanır. Şablondaki diğer ayarların çoğu dalga talebi stok yenilemesinde kullanılan şablonlardaki ayarlara benzer. Şablonda her madde ve yerleşim için bir satır olmalıdır. Stok yenilemeyi toplu iş kullanarak çalıştırdığınızda, sistem, satırların düzenlendiği sırayı kullanarak, stok yenilemenin gerekli olup olmadığını değerlendirir. 

Min/Maks stok yenileme stratejisinin madde için sabit yerleşim olarak ayarlanmamış boş yerleşimlerde stok yenilemesi yapamayacağını unutmayın. Stok yenilemesi yapılması gereken yerleşim sabit bir yerleşim değilse, sistem hangi maddenin stok yenilemesinin yapılacağını belirleyemez. Bu nedenle stok yenileme işlemi gerçekleşmeden önce eldeki miktarın en az bir kısmı gereklidir.

## <a name="load-demand-replenishment"></a>Yük talebi stok yenilemesi
Yük talebi stok birkaç yüke ait talebi toplar ve ilgili malzeme çekme yerleşimlerinde stok sağlamak için gerekli stok yenileme işini oluşturur. Yük talebi stok yenilemesi pek çok açıdan Dalga talep stok yenilemesine benzer. Aralarındaki temel fark Yük talebi stok yenilemesi ve Dalga talep stok yenilemesinin çalıştırıldığı durumlardır. Min/Maks stok yenileme gibi yük talebi stok yenilemesi toplu işlem kullanılarak çalıştırılır. Toplu iş ayarlamak için **Yük talebi stok yenilemesi** sayfasında, kullanılacak stok yenileme şablonunu seçin ve talebi belirlemek için kullanılacak yükleri belirten bir filtre sorgusu ayarlayın. Yerleşim sorgusu yüklerin toplam talebini karşılamak için kullanılabilir miktarın çıkarılacağı yerleşimleri belirler.

## <a name="immediate-replenishment"></a>Hemen yenileme
Talebi bir tahsisat işleminin sonunda toplamak ve stok yenilemeyi toplanmış miktarı temel alarak yapmak yerine, Hemen yenileme stratejisini uygulayabilirsiniz. Bu stratejiyi kullandığınızda, stok bir yerleşim yönergesi satırı başarısız olduğunda hemen yenilenebilir. Bu nedenle, stok yenilemeyi belirli birimlerle sınırlandırsa ve belirli konumlar için ayarlanmış miktarları kullanmak üzere ayarlayabilirsiniz.

## <a name="replenishment-prerequisites"></a>Stok yenileme önkoşulları

|      Önkoşul       |                                                                                                                                Tanım                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Madde           |                                                                                                        Madde mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.                                                                                                        |
|        Ambar        | Ambar mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir. Bir ambarı ambar yönetim süreçlerini etkinleştirmek üzere, <strong>Ambarlar</strong> sayfasında ambarı seçin, ardından <strong>Ambar yönetim süreçlerini kullan</strong> seçeneğini belirleyin. |
| Stok yenileme şablonları |                                                                   Min/Maks stok yenileme, Dalga talep stok yenilemesi veya Yük talebi stok yenilemesi için en az bir stok yenileme şablonu ayarlanmalıdır.                                                                   |
|        Konumlar        |                                                                                                       Yerleşimler oluşturulmalı ve bir yerleşim profiline bağlanmalıdır.                                                                                                       |
|    Konum profilleri    |                                                                                                        Yerleşim profilleri yerleşimleri oluşturmak için gereklidir.                                                                                                        |
|   Konum yönergeleri   |                                                       Yerleşim yönergeleri işi stok yenilemenin gerektiği yerleşimlere ve stok kaynağı olarak kullanılacak yerleşimlere yönlendirmek için gereklidir.                                                        |
|     İş şablonları      |                                                   <strong>Stok yenileme</strong> türünün iş şablonları stoğu istenen yerleşimlere taşıyabilmek üzere stok yenileme işi oluşturmak için gereklidir.                                                    |

