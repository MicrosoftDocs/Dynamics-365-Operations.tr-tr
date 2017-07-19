---
title: "Numara serilerine genel bakış"
description: "Microsoft Dynamics 365 for Finance and Operations'daki numara serileri, kimlik tanımlayıcıları gerektiren ana veri kayıtları ve hareket kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, <em>referans</em> olarak adlandırılır."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: d260f460bf0da072eb46909d8c28d18041ecaa78
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="number-sequence-overview"></a>Numara serilerine genel bakış

[!include[banner](../includes/banner.md)]


Microsoft Dynamics 365 for Finance and Operations'daki numara serileri, kimlik tanımlayıcıları gerektiren ana veri kayıtları ve hareket kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, <em>referans</em> olarak adlandırılır.

Microsoft Dynamics 365 for Finance and Operations'da bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz. Numara sıralarını ayarlamak için **Kuruluş yönetimi**'ndeki sayfaları kullanmanızı öneririz. Modüle özgü ayarları gerekiyorsa, bu modül içindeki referans için numara serileri belirtmek için bir modüldeki parametreleri sayfasını kullanabilirsiniz. Örneğin, **Alacak hesapları** ve **Borç hesapları**'nda, belirli müşteriler veya satıcılar için özel numara serileri tahsis etmek için numara serisi grupları ayarlayabilirsiniz. Bir numara sırası ayarlarsanız, hangi kuruluşun bu numara serisini kullanacağını tanımlayan bir kapsam belirtmelisiniz. Kapsam **Paylaşımlı**, **Şirket**, **Tüzel kişilik** veya **İşletim birimi** olabilir. **Tüzel kişilik** ve **Şirket**, **Mali takvim dönemi** kapsamları ile daha özel numara serileri oluşturmak için birleştirilebilir. Numara sırası biçimleri segmentlerden oluşur. **Paylaşımlı** dışında kapsamlara sahip seriler, kapsama karşılık gelen segmentler içerebilir. Örneğin, **Tüzel kişilik** kapsamını içeren bir numara serisi, bir tüzel kişilik segmenti içerebilir. Sayı dizisi biçiminde bir kapsam kesimi dahil ederek, numarasına bakarak belirli bir kaydın kapsamını tanımlayabilirsiniz. Segmentlere karşılık gelen kapsamların yanı sıra, numara sırası biçimleri **Sabit** ve **Alfasayısal parçaları** içerebilir. **Sabit** bir segment bir dizi değişmez harf, sayı veya simge kümesi içerir. Bir **Alfasayısal** segment, bir sayının kullanıldığı her seferde artan bir harf veya sayı kümesi içerir. Artan sayıları göstermek için (\#) ve artan harfleri göstermek için (&) simgelerini kullanın. Örneğin, \#\#\#\#\#\_2017 biçimi, 00001\_2017, 00002\_2017 sırasını ve devamını oluşturur.
Numara serisi örnekleri
------------------------

Aşağıdaki örnekler sıralı sayı biçimleri oluşturmak için segmentlerin nasıl kullanılacağını gösterir. Bu örnekler özellikle, kapsam segmentleri kullanmanın etkilerini gösterir.
### <a name="expense-report-numbers"></a>Gider raporu numaraları.

Aşağıdaki örnekte, **CS** başlıklı bir tüzel kişilik için gider raporu numaraları ayarlanır. **Alan:** Gider ve seyahat **Başvuru:** Gider raporu numarası **Kapsam:** Tüzel kişilik **Tüzel kişilik:** CS
| Segmentler  | Segment türü | Değer     |
|-----------|--------------|-----------|
| Segment 1 | Tüzel kişilik | CS        |
| Segment 2 | Sabit     | -GİDER- |
| Segment 3 | Alfasayısal | \#\#\#\#  |

**Biçimlendirilmiş sayı örneği**: CS-GİDER-0039 diğer tüzel kişilikler için de benzer bir numara sırası biçimi ayarlayabilirsiniz. Örneğin, **RW** adlı bir tüzel kişilik için, yalnızca tüzel kişilik segmentinin değerini değiştirirseniz, biçimlendirilmiş sayı RW-GİDER-0039 olur. Ayrıca, diğer tüzel kişilikler için de tam sayı dizisi biçimini değiştirebilirsiniz. Örneğin, Exp-0001 gibi biçimlendirilmiş bir sayı oluşturmak için bir tüzel kişilik kapsam segmentini atlayabilirsiniz.

### <a name="sales-order-numbers"></a>Satış sipariş numaraları

Aşağıdaki örnekte, şirket kodu **CEU** için satış siparişi numaraları ayarlanır. **Alanı:** Satış **Referans:** Satış siparişi **Kapsam:** Şirket **Şirket:** CEU
| Segmentler  | Segment türü | Değer    |
|-----------|--------------|----------|
| Segment 1 | Sabit     | SS-      |
| Segment 2 | Alfasayısal | \#\#\#\# |

**Örnek olarak biçimlendirilmiş sayı**: SO-0029 Kapsam segmenti biçime dahil edilmemiş bile olsa, her şirket kimliği için numaralandırma yeniden başlar. Tüm şirket kimlikleri için aynı biçimi kullanırsanız, her şirkette aynı numaraları kullanılır. Örneğin, satış siparişi numarası SO-0029, her şirkette kullanılır. Ayrıca, diğer şirket kimlikleri için de tam sayı dizisi biçimini değiştirebilirsiniz.

### <a name="purchase-requisition-numbers"></a>Satınalma talebi numaraları

Aşağıdaki örnekte, satınalma talebi sayıları kuruluş çapındadır. **Alanı:** Satınalma **Referans:** Satınalma talebi **Kapsam:** Paylaşılan
| Segmentler  | Segment türü | Değer    |
|-----------|--------------|----------|
| Segment 1 | Sabit     | Gereken      |
| Segment 2 | Alfasayısal | \#\#\#\# |

**Biçimlendirilmiş sayı örneği**: Req0052. Kapsamı **Paylaşılmış** olduğu için, numara sırası biçimi tüm organizasyonda kullanılır. Kuruluşun farklı bölümleri için farklı sayı sırası biçimleri ayarlayamazsınız.  Numara serilerinde performans ile ilgili hususlar
-----------------------------------------------

Numara serileri yapılandırmasını ayarlamadan önce sistem performansını nasıl etkileyebileceği hakkında aşağıdaki bilgileri göz önüne alın.
### <a name="continuous-and-non-continuous-number-sequences"></a>Sürekli ve sürekli olmayan numara serileri

Numara serileri sürekli veya sürekli olmayan şekillerde bulunabilir. Sürekli bir numara sırası hiçbir sayıyı atlamaz, ancak sayılar ardışık olarak kullanılamayabilir. Sürekli olmayan numara serisinden numaraları sıralı olarak kullanılır, ancak sıralama numaralar atlayabilir. Örneğin, bir kullanıcı bir hareketi iptal ederse, bir sayı oluşturulur fakat kullanılmaz. Devamlı bir numara sırasında bu sayı daha sonra tekrar kullanılır. Sürekli olmayan bir numara serisinde bu numara kullanılmaz. Sürekli numara serileri genellikle satınalma siparişleri, satış siparişleri ve faturalar gibi dış belgeler için gereklidir. Ancak, sürekli numara serileri, her yeni belge veya kayıt oluşturulduğunda numara için veritabanından yeni bir talep yapılması gerekeceği için sistem yanıt sürelerini olumsuz şekilde etkileyebilir. Sürekli olmayan bir numara serisi kullanırsanız, **Numara serileri** sayfasındaki **Performans** hızlı sekmesi üzerinde **Ön tahsisi** etkinleştirebilirsiniz. Ön tahsis edilecek bir numara miktarı belirttiğinizde, sistem bu numaraları seçer ve bellekte depolar. Ön tahsis edilen miktar kullanıldıktan sonra veritabanından yeni numaralar talep edilir. Sürekli numara sıraları kullanmak bir yasal gereklilik değilse, daha iyi performans için sürekli olmayan numara serileri kullanmanızı öneririz.

### <a name="automatic-cleanup-of-number-sequences"></a>Numara serilerinin otomatik temizlemesi

Güç kesintisi, bir uygulama hatası veya diğer beklenmeyen bir hata olması durumunda, sistem sürekli numara serileri için numaraların geri dönüşünü gerçekleştiremez. Kayıp numaraları kurtarmak için temizleme işlemini otomatik olarak veya el ile çalıştırabilirsiniz. Temizleme işlemi planlarken sunucu kullanımını dikkate alın. Temizleme işlemini yoğun olmayan saatlerde toplu iş olarak gerçekleştirmenizi öneririz.






