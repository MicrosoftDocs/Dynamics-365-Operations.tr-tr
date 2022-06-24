---
title: Özellik kurulumları ile çalışma
description: Bu makalede, Elektronik faturalama özelliklerinin nasıl ayarlanacağı açıklanmaktadır.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23466a53bb8ba597503aaa12d41395fc82b9f14e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904339"
---
# <a name="work-with-feature-setups"></a>Özellik kurulumları ile çalışma

[!include [banner](../includes/banner.md)]

Elektronik dosyalar ve diğer işleme adımlarını (örneğin dosyaları dijital olarak imzalamak, bunları kamu web hizmetlerine göndermek ve yanıt almak ya da bunları saklamak) kurmak, işlem ardışık düzeni kurmak, geçerlilik kuralları belirlemek ve Elektronik faturalama özellikleri için değişkenler ayarlamak için.

Kurulum bilgileri, *özellik kurulum* kavramında birleştirilir ve oluşturulabilir, silinebilir, ayarlanabilir. Elektronik faturalama özelliklerinin tamamlanan sürümleri için bilgiler de görüntülenebilir.

Elektronik dosyaları oluşturmak, işlemek ve almak için farklı senaryolar tanımlamak zorunda olduğunuz birçok özellik kurulum maddesi oluşturabilirsiniz. Bu özellik kurulum öğelerinin yürütme için bağımsız işlem eylemleri ve koşulları olmasına karşın, tek bir elektronik faturalama özelliğinin parçası olarak oluşturulur ve bunun yaşam döngüsü ve dağıtım işlemi devralınır.

## <a name="add-a-feature-setup"></a>Özellik kurulumu ekleme

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Elektronik faturalama özellikleri** sayfasında, **Taslak** durumuna sahip olan bir Elektronik faturalama özelliği sürümü seçin.
4. **Kurulumlar** sekmesinde **Ekle**'yi seçin.
5. **Özellik kurulumu oluştur** açılan iletişim kutusunda **Yeni** alan grubunda aşağıdaki seçeneklerden birini belirleyin:
 
    - **Özel kurulum** – Kurulum türüne bağlı olarak, boş kanalları bulunan yeni bir özellik kurulumu, boş bir işlem ardışık düzen listesi, uygulanabilirlik kuralları için boş bir bölüm ve varsayılan değişkenler kümesi oluşturun.
    - **Özellik kurulumundan** – Geçerli elektronik faturalama özelliğinin kapsamında başka bir özellik ayarının kopyasını oluşturun.

6. Son adımda **Özel kurulum** seçeneğini belirlediyseniz, özellik kurulum maddesi için bir ad ve açıklama girin ve **Kurulum türü** alan grubunda aşağıdaki seçeneklerden birini belirleyin:

    - **İşleme ardışık düzeni** – Giden elektronik belgeleri oluşturmak ve işlemek için bu seçeneği belirleyin. Bu kurulum türü için, sistem boş bir işlem kanalı listesi, uygulanabilirlik kuralları için boş bir bölüm ve varsayılan değişkenler kümesi oluşturur. Gelen elektronik belgelerin kanallarıyla çalışamazsınız.
    - **Veri kanalı**: Tanımlı kanalların birinden gelen elektronik belgeleri alma ve bunları doğrudan Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'a ek eylemler olmadan aktarma sürecini ayarlamak için bu seçeneği belirleyin. Bu kurulum türü için sistem, veri kanalları için önceden belirlenmiş parametre listesi, geçerlilik kuralları için boş bir bölüm ve varsayılan değişkenler kümesi oluşturur. İşlem ardışık düzenine herhangi bir eylem ekleyemezsiniz.
    - **Veri kanalı ve işlem ardışık düzeni** – Bu kurulum türü **Veri kanalı** kurulum türüne benzer. Ancak, Finance veya Supply Chain Management'a gelen elektronik belge geçirilmeden önce, işlem kanalında ek eylemler ayarlayabilirsiniz.

7. Son adımda **Veri kanalı** veya **Veri kanalı ve işlem ardışık düzen** seçeneğini belirlediyseniz, **Veri kanalı seç** alanında, tümleştirilecek kanalı seçmeniz gerekir.
8. **Oluştur**'u seçin.

Bir özellik kurulumu oluşturulduktan sonra, bunu konfigüre etmek için **Düzenle**'yi seçebilirsiniz.

## <a name="edit-a-feature-setup"></a>Özellik kurulumu düzenleme

Özellik ayarının türüne bağlı olarak, giden elektronik dosyaları oluşturma ve bunları harici kanallara gönderme veya gelen belgeleri alma ve Finance veya Supply Chain Management uygulamanıza geçirme işlemini konfigüre edebilirsiniz.

### <a name="data-channel"></a>Veri kanalı

Bir *veri kanalı*, elektronik dosyayı alır ve bunu işler ya da doğrudan Finance veya Supply Chain Management'a geçirir. Bu seçenek, **İşlem ardışık düzen** türünün özellik kurulumları için kullanılamaz.

Bir veri kanalı ayarlamak için kanalın adını girin. Sonra, seçilen kanal türüne göre parametreleri tanımlayın. Veri kanalı tanımlayıcısı, veri kanalını tanımlamak için özel olarak oluşturulan değişkene başvurmalıdır. Finance veya Supply Chain Management'ta referans olarak kullanılacaktır.

**Ekler filtresi** sekmesinde, belirli dosyaları kanaldan almak için filtre kümesi tanımlamanız gerekir. Dosyaların farklı dosya adı uzantılarına sahip olmasını bekliyorsanız veya dosyaların dosya adına göre farklı işlenmelerini istiyorsanız, birkaç satır oluşturabilirsiniz. Ana parametreler aşağıdadır:

- **Ad** – İşlem sırasında sistemin başvurabileceği dosyanın adını girin. Finance ve Supply Chain Management uygulamalarında, gönderme günlüğündeki dosyaları görebileceksiniz.
- **Filtre** – Dosyaları seçmek için filtreyi tanımlayın.
- **İsteğe bağlı** - Bu onay kutusu temizlenirse dosya gereklidir. Bu durumda, kanallar filtreye karşılık gelen dosyalar içermiyorsa sistem bir hata iletisi görüntüler. Bu parametre, e-postalara uygulanabilir.

Kanal bir posta kutusu ise ve gelen e-postada birkaç ek varsa, hizmetin ekleri nasıl işleyeceğini tanımlamak için kuralları yapılandırabilirsiniz. Hizmet, her bir eki ayrı bir elektronik fatura olarak kabul edebilir veya bir eki bir ana fatura, diğer tüm ekler ise eklemeler olarak kabul edebilir.

### <a name="processing-pipeline"></a>İşlem yapılan işlem hattı

*İşlem ardışık düzeni*, başarılı şekilde tamamlanana kadar sırayla çalıştırılan *eylemler* kümesidir. Bir işlem ardışık düzeni kullanarak, elektronik dosyaları oluşturma ve diğer adımları gerçekleştirme sürecini ayarlayabilirsiniz (örneğin, dosyaları dijital olarak imzalama, harici web hizmetlerine gönderme ve yanıtı ayrıştırma ve gelen belgeleri alma ve işleme).

Eylemler listesi önceden tanımlanmıştır. Belgeleri göndermek ve teslim etmek için gerekli işlemi mantıksal olarak tanımlayan eylemlerin birleşimini belirtmek için **Yeni** ve **Sil** düğmelerini kullanabilirsiniz.

Eylemlerin sırası önemlidir. Sırayı, **Yukarı** ve **Aşağı** düğmelerini kullanarak ayarlayabilirsiniz.

Her eylemin konfigüre edebilir veya ayarlayabileceğiniz bir dizi parametresi vardır. Belirli parametre kümesi, eylemin türüne bağlıdır.

- **Eylem** – Eylem türünü seçin.
- **Eylem adı** – Eylem adını girin. Bu ad, gönderme günlüklerinde ve Finance ve Supply Chain Management uygulamalarındaki iletilerde görünür.
- **Açıklama** – İşlemdeki eylemin amacı hakkında daha fazla ayrıntı sağlar.
- **Yeniden denemeyi etkinleştir** – Bu onay kutusunu işaretlerseniz, **Eylemi yeniden dene** alanında bir eylem seçebilir ve ek parametreleri **Yeniden deneme parametreleri** sekmesinde konfigüre edebilirsiniz.

    Yeniden deneme işlevi, belirli bir eylem çalışmazsa hizmetin davranışını yapılandırmanızı sağlar. Örneğin, bağlanmaya çalıştığınız harici web hizmeti yanıt vermiyorsa, sistemin bağlantıyı kaç kez yeniden yapması gerektiğini, hangi aralığı ve işlem ardışık düzeninde hangi eylemi yapacağını belirleyebilirsiniz.

- **Dışa aktarma sonuçları** – İşlem ardışık düzenindeki *bir* eylem için bu onay kutusunu seçebilirsiniz. Eylemin Finance veya Supply Chain Management uygulamasında ürettiği elektronik dosya daha sonra **Elektronik belgeler gönderme günlüğü** sayfasından dışa aktarılabilir.

### <a name="applicability-rules"></a>Uygulanabilirlik kuralları

*Geçerlilik kuralları*, Elektronik Faturalama özellik kümesi üzerinden çalışan Elektronik faturalama özellikleri için bağlam sağlayan yapılandırılabilir cümleciklerdir.
Finance veya Supply Chain Management'tan Elektronik faturalamaya gönderilen iş belgelerinde, Elektronik Faturalama özelliğinin gönderiyi işlemesini sağlayacak belirli bir Elektronik faturalma özelliği ve belirli bir özellik kurulum öğesine olanak tanıyacak açık bir referans bulunmaz. Ancak, bir iş belgesi doğru şekilde yapılandırıldığında, Elektronik faturalamanın, hangi Elektronik faturalama özelliği sürümü ve işleme ardışık düzeninin seçilip çalıştırılması gerektiğine karar vermesini sağlayan gerekli öğeleri içerir.

Geçerlilik kuralları sayesinde Elektronik Faturalama hizmeti, bir gönderiyi işlemek için kullanılmasını gereken spesifik Elektronik faturalama özelliklerini bulabilir. Doğru özellikleri bulmak için, gönderilen iş belgesindeki **Bağlam** alanları uygulanabilirlik kurallarından alınan yan tümceciklerine göre eşleştirilir.

Geçerlilik kurallılıklarıyla aşağıdaki yollarla çalışabilirsiniz:

- Uygulanabilirlik kuralları kümesine yeni bir yan tümce eklemek için **Yeni**'yi seçin.
- Bir yan tümceyi silmek için **Sil**'i seçin.
- Birden fazla kayıt seçin ve bir madde veya mantıksal ifadeler birleşimi oluşturmak için **Gruplandır** veya **Grubu boz** düğmesini kullanın. Örneğin, gruplandırmak istediğiniz satırları seçin ve **Yan tümceyi gruplandır**'ı seçin. Yan tümceler gruplandırıldığında, kılavuza yeni bir sütun eklenir. Bu sütun gruplanmış yan tümce için mantıksal işleci belirtir. Aşağıdaki işleçler desteklenmektedir:

    - Equal
    - Not equal
    - Büyüktür/küçüktür
    - Büyük veya eşit / Küçük veya eşit
    - Contains
    - Şununla başla

    > [!NOTE]
    > Bir yan tümcenin grubunu çözdüğünüzde, her zaman en içteki gruplandırma düzeyinden başlayın.

### <a name="variables"></a>Değişkenler

*Değişkenler*, işlem ardışık düzeni ayarlarken ve eylemler arasında veri akışı yaparken size daha fazla esneklik sağlar. Verileri veya elektronik dosyaları geçici olarak saklamak için bazı eylem parametrelerinde bir değişkene başvurabilirsiniz. Bazı değişkenler, Finance veya Supply Chain Management uygulamaları ile elektronik faturalama servisi arasında veri iletmek için kullanılır.

Sistem, varsayılan olarak bazı değişkenler oluşturur. Örneğin, **BusinessDocumentDataModel** değişkeni, gönderme işlemi sırasında bağlı uygulamadan gelen çağrı içinde bulunan bir JavaScript Nesne Gösterimi (JSON) yapısı içindeki iş verilerini içerir.

Aşağıdaki değişken tipleri mevcuttur:

- **Sabit** - Ardışık düzen eylemlerini işlemek için kullanılan geçici verileri depolayan kapsayıcı.
- **İstemciden** – Dynamics 365 istemcisinden gönderme işlemi yürütüldüğünde değişkenin içeriği alınır.
- **İstemciye** – Değişken içeriği, Dynamics 365 istemcisi tarafından gönderme işlemi çalıştırıldığında içe aktarılabilir hale getirilir.
- **Veri türü** - Değişkende depolanan bilgilerin veri türünü seçin.

### <a name="parameters"></a>Parametreler

**İş verileri azaltmayı devre dışı bırak** seçeneği, elektronik belge gönderme sırasında Finance veya Supply Chain Management uygulamasından gelen iş verileri yükünün yapısını en iyi duruma getirmek için kullanılır. Optimizasyon, gerekli elektronik dosyaya daha fazla dönüşüm için elektronik faturalama hizmetine giden verilerin azaltılmasına yardımcı olur. Varsayılan değer **Hayır** değeridir.

- **Evet** – Finance veya Supply Chain Management **Elektronik raporlama** modülünde tanımlanan **Fatura modeli** veya **Mali model** (Brezilya için) yapısına ait bir JSON dosyası gönderir. Modelin tüm öğeleri, son elektronik dosya yapısından bağımsız olarak, uygulama tarafındaki iş verileriyle doldurulur. Modeller genellikle hedef dosya yapısının gerektirdiğinden daha fazla iş verisi içerir ve uygulamada bu verileri oluşturmak için daha fazla zaman gerekebilir. Nadiren de olsa, bir elektronik faturalama özellik ve özellik kurulumunda farklı çıkış dosyaları oluşturmak isteyebileceğiniz nadir bir olayda bu seçenek için **Evet** değeri gereklidir. Senaryolarınız, elektronik dosyaların yapısı ve iş verilerinin bilgileri hakkında sorun giderirken **Evet** değeri yararlıdır.
- **Hayır** – Finance veya Supply Chain Management, iş verileri olmadan hizmete ilk çağrı yapar. Bu çağrının amacı, işlem ardışık düzeninde elektronik dosya dönüşümü için kullanılacak elektronik raporlama (ER) yapılandırmasıyla ilgili bilgi almak içindir. Bu bilgiler, uygulamanın, **Fatura modeli** veya **Mali model** (Breziya için) yapısı JSON dosyasına eklenmesi gereken iş verilerinin alt kümesini belirlemek için kullandığı uygulamaya iade edilir. Bu seçenek için **Hayır** değeri, uygulamanın hizmete teslim aldığı iş verilerinin hacmini azaltmaya yardımcı olur çünkü uygulama yalnızca bir elektronik dosyayı başarıyla üretmek için gereken iş verilerini gönderebilir.

### <a name="validate-a-feature-setup"></a>Bir özellik kurulumunu doğrulama

Tüm yapılandırmanın tutarlılığını kontrol etmek için doğrulama çalıştırabilirsiniz. Örneğin, eylem için zorunlu bir parametre boş bırakılmışsa doğrulama işlemi bu tutarsızlığı algılar ve bir uyarı iletisi verir.

- **Özellik sürümü kurulumu** sayfasında, Eylem bölmesinde, **Doğrula**'yı seçin.

## <a name="delete-a-feature-setup"></a>Bir özellik kurulumunu silme

1. **Elektronik faturalama özellikleri** sayfasında, **Taslak** durumuna sahip olan bir elektronik faturalama özelliği sürümü seçin.
2. **Kurulumlar** sekmesinde **Sil**'i seçin.
3. Görüntülenen ileti kutusunda, özellik kurulumunu silmek istediğinizi onaylamak için **Evet**'i seçin.
