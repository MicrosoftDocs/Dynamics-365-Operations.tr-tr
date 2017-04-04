---
title: "Numara serilerine genel bakış"
description: "Microsoft Dynamics 365 işlemleri için numara serilerini ana veri kayıtları ve tanımlayıcıları gerektiren işlem kayıtları okunabilir ve benzersiz tanımlayıcılarını oluşturmak için kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, <em>referans</em> olarak adlandırılır."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a812c93a13fd36f44e659c9976099af62793098f
ms.lasthandoff: 03/31/2017


---

# <a name="number-sequence-overview"></a>Numara serilerine genel bakış

Microsoft Dynamics 365 işlemleri için numara serilerini ana veri kayıtları ve tanımlayıcıları gerektiren işlem kayıtları okunabilir ve benzersiz tanımlayıcılarını oluşturmak için kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, <em>referans</em> olarak adlandırılır.

Microsoft Dynamics 365 işlemleri için yeni kayıtlar için bir başvuru oluşturmak için önce bir numara sırası oluşturun ve başvuru ile ilişkilendirin. Numara sıralarını ayarlamak için **Kuruluş yönetimi**'ndeki sayfaları kullanmanızı öneririz. Modüle özgü ayarları gerekiyorsa, bu modül içindeki referans için numara serileri belirtmek için bir modüldeki parametreleri sayfasını kullanabilirsiniz. Örneğin, **Alacak hesapları** ve **Borç hesapları**'nda, belirli müşteriler veya satıcılar için özel numara serileri tahsis etmek için numara serisi grupları ayarlayabilirsiniz. Bir numara sırası ayarlarsanız, hangi kuruluşun bu numara serisini kullanacağını tanımlayan bir kapsam belirtmelisiniz. Kapsam **Paylaşımlı**, **Şirket**, **Tüzel kişilik** veya **İşletim birimi** olabilir. **Tüzel kişilik** ve **Şirket**, **Mali takvim dönemi** kapsamları ile daha özel numara serileri oluşturmak için birleştirilebilir. Numara sırası biçimleri segmentlerden oluşur. **Paylaşımlı** dışında kapsamlara sahip seriler, kapsama karşılık gelen segmentler içerebilir. Örneğin, **Tüzel kişilik** kapsamını içeren bir numara serisi, bir tüzel kişilik segmenti içerebilir. Sayı dizisi biçiminde bir kapsam kesimi dahil ederek, numarasına bakarak belirli bir kaydın kapsamını tanımlayabilirsiniz. Segmentlere karşılık gelen kapsamların yanı sıra, numara sırası biçimleri **Sabit** ve **Alfasayısal parçaları** içerebilir. **Sabit** bir segment bir dizi değişmez harf, sayı veya simge kümesi içerir. Bir **Alfasayısal** segment, bir sayının kullanıldığı her seferde artan bir harf veya sayı kümesi içerir. Sayı işareti kullanın (\#) artan harflerle için artan bir sayı ve bir ampersan göstermek için (&). Örneğin, Biçim \#\#\#\#\#\_2017 00001 sırası oluşturur\_, 2017 00002\_2017 vb..
Numara serisi örnekleri
------------------------

Aşağıdaki örnekler sıralı sayı biçimleri oluşturmak için segmentlerin nasıl kullanılacağını gösterir. Bu örnekler özellikle, kapsam segmentleri kullanmanın etkilerini gösterir.
### <a name="expense-report-numbers"></a>Gider raporu numaraları.

Aşağıdaki örnekte, **CS** başlıklı bir tüzel kişilik için gider raporu numaraları ayarlanır. **Alan: **Gider ve seyahat **Başvuru: **Gider raporu numarası **Kapsam: **Tüzel kişilik **Tüzel kişilik: **CS
| Segmentler  | Segment türü | Değer     |
|-----------|--------------|-----------|
| Segment 1 | Tüzel kişilik | CS        |
| Segment 2 | Sabit     | -GİDER- |
| Segment 3 | Alfasayısal | \#\#\#\#  |

**Biçimlendirilmiş sayı örneği**: CS-GİDER-0039 diğer tüzel kişilikler için de benzer bir numara sırası biçimi ayarlayabilirsiniz. Örneğin, **RW** adlı bir tüzel kişilik için, yalnızca tüzel kişilik segmentinin değerini değiştirirseniz, biçimlendirilmiş sayı RW-GİDER-0039 olur. Ayrıca, diğer tüzel kişilikler için de tam sayı dizisi biçimini değiştirebilirsiniz. Örneğin, Exp-0001 gibi biçimlendirilmiş bir sayı oluşturmak için bir tüzel kişilik kapsam segmentini atlayabilirsiniz.

### <a name="sales-order-numbers"></a>Satış sipariş numaraları

Aşağıdaki örnekte, şirket kodu **CEU** için satış siparişi numaraları ayarlanır. **Alanı: **Satış **Referans: **Satış siparişi **Kapsam: **Şirket **Şirket: **CEU
| Segmentler  | Segment türü | Değer    |
|-----------|--------------|----------|
| Segment 1 | Sabit     | SS-      |
| Segment 2 | Alfasayısal | \#\#\#\# |

**Örnek olarak biçimlendirilmiş sayı**: SO-0029 Kapsam segmenti biçime dahil edilmemiş bile olsa, her şirket kimliği için numaralandırma yeniden başlar. Tüm şirket kimlikleri için aynı biçimi kullanırsanız, her şirkette aynı numaraları kullanılır. Örneğin, satış siparişi numarası SO-0029, her şirkette kullanılır. Ayrıca, diğer şirket kimlikleri için de tam sayı dizisi biçimini değiştirebilirsiniz.

### <a name="purchase-requisition-numbers"></a>Satınalma talebi numaraları

Aşağıdaki örnekte, satınalma talebi sayıları kuruluş çapındadır. **Alanı: **Satınalma **Referans: **Satınalma talebi **Kapsam: **Paylaşılan
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




