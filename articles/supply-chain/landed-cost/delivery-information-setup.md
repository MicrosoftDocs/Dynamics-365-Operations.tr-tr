---
title: Teslimat bilgileri ayarı
description: Bu konuda, Varış yeri maliyeti modülü için teslimat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a0b510e4f58ca1cfec940093d118618693c68d38
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694697"
---
# <a name="delivery-information-setup"></a>Teslimat bilgileri ayarı

[!include [banner](../../includes/banner.md)]

Bu konuda, **Varış yeri maliyeti** modülü için teslimat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="shipping-ports"></a>Sevkiyat limanları

Sevkiyat limanları, malların nereden ve nereye sevk edildiğini belirler. Her seyahat için bir "varış" limanı ve bir "çıkış" limanı, seyahat gemisi için seçilen yolculuğa göre tanımlanır. Sevkiyat limanları, bir yolculuğun durakları ve ayrıca seyahat etkinliklerini oluşturmak için kullanılır. Bunlar genellikle şehrin ve fiziksel sevkiyat limanının bulunduğu ülke veya bölgenin adı kullanılarak tanımlanır.

Sevkiyat limanlarıyla çalışmak için **Varış yeri maliyeti \> Teslimat bilgileri kurulumu \> Sevkiyat limanları**'na gidin. Burada, sevkiyat limanlarınızın kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Sevkiyat limanı | Sevkiyat limanı için benzersiz bir tanımlama adı/numarası girin. |
| Tanım | Sevkiyat limanı için açıklama girin. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>İzleme denetim merkezi

Sevkiyat konteynerleri bir duraktan diğerine geçerken bir seyahatle ilişkili sağlama sürelerini, durum güncelleştirmelerini ve bilgi akışını ayarlamak için İzleme denetim merkezini kullanırsınız. İzleme denetimi kaydı oluşturduğunuzda, bu kayıt bir seyahat için yolculuğun belirli bir durağıyla ilişkilidir. Bir seyahat, bir durağı güncelleştirdiğinde, ilişkili kayıt güncelleştirilir ve tanımlandığı gibi doldurulur. **Tüm seyahatler** sayfasından bireysel yolculuklar için izleme bilgilerini güncelleştirebilirsiniz.

İzleme denetim merkezini açmak için **Varış yeri maliyeti \> Teslimat bilgileri kurulumu \> İzleme denetim merkezi**'ne gidin.

İzleme denetim merkezi, liste bölmesindeki **Oluşturma türü** alanında seçilen değere bağlı olarak üç sayfa görüntülemeden birini gösterir: *Boş*, *Sağlama süresi* veya *Durum güncelleştirmesi*. Her oluşturma türü, bir seyahatin başlangıç noktasından son hedefe ilerlemesiyle ilişkili farklı bir bilgi kümesini güncelleştirir.

### <a name="common-rule-settings"></a>Ortak kural ayarları

Aşağıdaki tabloda, İzleme denetim merkezindeki her üç oluşturma türü için de kullanılabilen alanlar gösterilmektedir.

| Alan | Tanım |
|---|---|
| Kaynak tablo, Kaynak alan | Bu alanlar veritabanındaki bir kaynak tablo ve alanı tanımlar. Kural, değeri alana yükler ve sonra kuralın diğer ayarları tarafından tanımlanan şekilde kullanır. |
| Hedef tablo, Hedef alan | Bu alanlar veritabanındaki bir hedef tablo ve alanı tanımlar. Kural, değeri alana yükler ve sonra kuralın diğer ayarları tarafından tanımlanan şekilde kullanır (veya üzerine yazar). |
| Faaliyet | Bu alan, bir kuralla eşleşen bir sevkiyat konteynerine uygulanması gereken etkinlik türünü tanımlar. |
| Eşleştirme ölçütü | Bu alan, sistemin bir kural eşleşmesini nasıl tanımladığını belirler. Her durumda, sistem, hedef tabloda bir alanın güncelleştirilip güncelleştirilmeyeceğini ve ne zaman güncelleştirileceğini belirlemek için kaynak ve hedef tablolardaki verileri gözden geçirir.<p>Örneğin, kaynak tablo *Seyahatler* ve hedef tablo *Satın alma başlığı* veya *Satın alma satırları*'dır. *Seyahatler* tablosunda *Hong Kong* **Çıkış limanı** değerine ve *Satın alma başlığı* tablosu *Şanghay* **Çıkış limanı** değerine sahiptir. Daha sonra *Hong Kong* "çıkış" limanı olarak gösteren bir kural oluşturulur. Bu durumda, **Eşleştirme ölçütleri** alanının değerleri aşağıdaki şekilde çalışır:</p><ul><li>**Her ikisi**: İki limandan biri eşleşmediği için hedef alan güncelleştirilmez.</li><li>**Kaynak**: Kaynak tablonun "çıkış" limanı *Hong Kong* olduğundan, hedef alan güncelleştirilir.</li><li>**Hedef**: Hedef tablonun "çıkış" limanı *Şanghay* (*Hong Kong* değil) olduğundan hedef alan güncelleştirilmez.</li></ul> |
| Eylemi kopyala | Kullanılabilir değerler *Kopyala* ve *Varsayılan*'dır. Kaynak alandaki değeri hedef alana kopyalamak için *Kopyala*'yı seçin. Hedef alan için statik bir değer ayarlamak üzere *Varsayılan*'ı seçin. |
| Varsayılan | **Kopyalama eylemi** alanı *Varsayılan* olarak ayarlandığında, **Varsayılan** alan hedef alanın varsayılan değerini tanımlar. Örneğin, eylem bir liman güncelleştirmesi ile ilişkiliyse ve **Kopyalama eylemi** alanı *Varsayılan* olarak ayarlanmışsa **Varsayılan** alanı, bir limanı tanımlar. |
| Durak | Bu alan, yükleme veya gümrük gibi belirtilen eylemin gerçekleştiği yolculuk durağını tanımlar. |
| Hizmet sağlayıcı | Yolculuğun geçerli durum güncelleştirmesi/durağı için belirli bir servis sağlayıcısı kullanılıyorsa bu alan servis sağlayıcısını tanımlar. Servis sağlayıcılar satıcı hesabında tanımlanır. |

### <a name="lead-time-rules"></a>Sağlama süresi kuralları

Sağlama süresi, bir seyahatin, bir yolculuk için tanımlanmış bir durağı tamamlamak için gereken tahmini süredir. Bir yolculuğun her durağının sağlama süresi, seyahatin tahmini teslimat tarihini hesaplamak için kullanılır. Bu tarih daha sonra seyahatteki her satın alma satırındaki **Onaylanan teslim tarihi** alanına girilir.

Tarih güncelleştirmelerini yönetmek için sağlama süresi kurallarını kullanırsınız. Bir seyahat için bir yolculuk şablonu kullanıldığında etkinlikler otomatik olarak oluşturulur.

İzleme denetim merkezine sağlama süresi kuralı eklemek için şu adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Varış yeri maliyeti \> Çok duraklı yolculuk kurulumu \> Duraklar**'a gidin. Sağlama sürelerini ayarlamak istediğiniz durağı seçin ve sonra Eylem Bölmesinde **İzleme denetim merkezi**'ni seçin. İzleme denetim merkezi, seçilen durak hakkındaki bilgilerle önceden yüklenmiştir.
    - **Varış yeri maliyeti \> Teslimat bilgileri kurulumu \> İzleme denetim merkezi**'ne gidin. Daha sonra bu yordamın 4. adımında el ile bir durak seçin.

1. Liste bölmesinde, **Oluşturma türü** alanını *Sağlama süresi* olarak ayarlayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. 1. adımdaki İzleme denetim merkezinden başladıysanız **Durak** alanını sağlama süresi kuralı oluşturmak istediğiniz durağa ayarlayın. **Duraklar** sayfasından başladıysanız **Durak** alanı İzleme denetim merkezini açmadan önce seçtiğiniz durağa önceden ayarlanmıştır.

    **Durak** alanının değerine bağlı olarak burada gösterildiği gibi birkaç alan otomatik olarak ayarlanır:

    - **Kaynak tablo:** *Konteyner etkinlikleri*
    - **Kaynak alan:** *Başlangıç tarihi*
    - **Hedef tablo:** *Konteyner etkinlikleri*
    - **Hedef alan:** *Tahmini bitiş tarihi*

1. **Etkinlik** alanında, mevcut kuralın geçerli olması gereken etkinliği seçin.
1. **Sağlama süresi** alanına, geçerli kural tetiklendiğinde uygulanması gereken sağlama süresini (gün olarak) girin.

### <a name="status-update-rules"></a>Durum güncelleştirmesi kuralları

**Oluşturma türü** alanının *Durum güncelleştirmesi* olarak ayarlandığı kayıtlar, satın alma siparişi satırlarının durumunu veya yolculuk, sevkiyat konteyneri veya folyo düzeyindeki durumu güncelleştirir. Durumlar bağımsız olarak ayarlanabilir. Bir seyahatin aşaması (alınan belgeler veya transitteki mallar gibi) hakkında kullanıcıyı veya departmanı bilgilendirmek için bunları kullanın.

**Oluşturma türü** alanı *Durum güncelleştirmesi* olarak ayarlandığında, İzleme denetim merkezi, maliyet alanını ve seyahatin güncelleştirilmiş durumunu tanımlayabileceğiniz bir **Satırlar** hızlı sekmesi içerir. Örneğin, **Maliyet alanı** alanının *Konteyner* olarak ayarlandığı ve **Seyahat durumu** alanının *Transitteki mallar* olarak ayarlandığı bir satırınız vardır. Bu durumda, bir sipariş belirtilen durağı tamamladığında, sevkiyat konteynerinin **Seyahat durumu** alanı *Transitteki Mallar* olarak güncelleştirilir.

Durum güncelleştirmeleri, seyahatle ilişkili yolculuk satırları ve satın alma siparişi satırlarında bu seyahatin durumunu sağlar. Bir seyahat limandan, seyir ve gümrükten hedef depoya doğru ilerlerken, seyahat kaydının **Seyahat durumu** alanı, öğelerin bulunduğu aşamanın hızlı bir görünümünü sağlar.

İzleme denetim merkezine durum güncelleştirme kuralı eklemek için şu adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Varış yeri maliyeti \> Çok duraklı yolculuk kurulumu \> Duraklar**'a gidin. Durum güncelleştirmesi ayarlamak istediğiniz durağı seçin ve eylem bölmesinde **İzleme denetim merkezi**'ni seçin. İzleme denetim merkezi, seçilen durak hakkındaki bilgilerle önceden yüklenmiştir.
    - **Varış yeri maliyeti \> Teslimat bilgileri kurulumu \> İzleme denetim merkezi**'ne gidin. Daha sonra bu yordamın 4. adımında el ile bir durak seçin.

1. Liste bölmesinde, **Oluşturma türü** alanını *Durum güncelleştirmesi* olarak ayarlayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. 1. adımdaki İzleme denetim merkezinden başladıysanız **Durak** alanını durum güncelleştirme kuralı oluşturmak istediğiniz durağa ayarlayın. **Duraklar** sayfasından başladıysanız **Durak** alanı İzleme denetim merkezini açmadan önce seçtiğiniz durağa önceden ayarlanmıştır.

    **Durak** alanının değerine bağlı olarak burada gösterildiği gibi birkaç alan otomatik olarak ayarlanır:

    - **Kaynak tablo:** *Konteyner etkinlikleri*
    - **Kaynak alan:** *Fiili bitiş tarihi*
    - **Hedef tablo:** Bu alan boş bırakılır.
    - **Hedef alan:** Bu alan boş bırakılır.

1. **Etkinlik** alanında, kuralınızın geçerli olması gereken etkinliği seçin.
1. **Satırlar** hızlı sekmesinde, her maliyet alanı için durum güncelleştirmelerini girin.

### <a name="blank-type-rules"></a>Boş tür kuralları

Başka bir alanın verilerini temel alan bir alan değerini geçersiz kılmak veya girmek için **Oluşturma türü** değeri *Boş* olan kayıtları kullanırsınız. Varış yeri maliyetindeki bir alan, İzleme denetim merkezinde ayarlanan kurallara bağlı olarak Microsoft Dynamics 365 Supply Chain Management'ın diğer alanlarındaki verilerin üzerine yazar.

1. **Varış yeri maliyeti \> Teslimat bilgileri kurulumu \> İzleme denetim merkezi**'ne gidin.
1. Liste bölmesinde, **Oluşturma türü** alanını *Boş* olarak ayarlayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Kuralınız için gerektiği gibi kaynak ve hedef değerleri, eşleşen ölçütleri, kopyalama eylemini ve diğer ilgili parametreleri tanımlayın.

### <a name="required-tracking-control-setup"></a>Gerekli izleme denetimi kurulumu

Her yolculuk şablonu için İzleme denetim merkezinde iki kayıt ayarlanmalıdır. Bu kayıtların her ikisi de *Boş* **Oluşturma türü** değerine sahiptir ve tüm Varış yeri maliyeti uygulamalarında kullanılır. Satın alma onaylanma tarihin ve transitteki malların beklenen tarihleri seyahatler için ve ilgili satın alma siparişi satırlarında beklenen şekilde güncelleştirilmesine yardımcı olurlar.

Satın alma satırlarını güncelleştirmek için ilk kayıt gereklidir. Aşağıdaki ayarlara sahip olmalıdır:

- **Kaynak tablo:** *Konteyner etkinlikleri*
- **Kaynak alan:** *Tahmini bitiş tarihi*
- **Hedef tablo:** *Satın alma satırları*
- **Hedef alan:** *Onaylanan tarih veya teslimat tarihi*

İkinci kayıt, transitteki mal hareketlerini güncelleştirmek için gereklidir. Aşağıdaki ayarlara sahip olmalıdır:

- **Kaynak tablo:** *Konteyner etkinlikleri*
- **Kaynak alan:** *Tahmini bitiş tarihi*
- **Hedef tablo:** *Transitteki mal siparişi*
- **Hedef alan:** *Beklenen tarih*
