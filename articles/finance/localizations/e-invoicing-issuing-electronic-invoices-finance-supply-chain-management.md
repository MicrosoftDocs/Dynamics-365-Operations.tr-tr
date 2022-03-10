---
title: Finance ve Supply Chain Management'ta elektronik fatura kesme
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında Elektronik faturalama üzerinden nasıl elektronik fatura kesileceğini açıklamaktadır.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 24909c2a2505724c159e939535c1d57cb66e48629862bebb32b3d72c0eb06c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752138"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management'ta elektronik fatura kesme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında Elektronik faturalama üzerinden nasıl elektronik fatura kesileceğini açıklamaktadır.


## <a name="feature-activation"></a>Özellik etkinleştirme

Elektronik faturalama ile elektronik faturalar kesmek için, Finance ve Supply Chain Management'ta Özellik referansını etkinleştirmelisiniz.

Her özellik bir ülke/bölge ile ilgili elektronik faturalama gereksinimlerini karşılayan belirli bir elektronik faturalama özelliğine karşılık gelir.

Aşağıdaki tabloda, elektronik faturalamanın destekleyebileceği Özelliklerin listesi gösterilmektedir.

| Kuruluş adı                                              | Ülke/bölge |
|---------------------------------------------------|----------------|
|Avusturya'ya özgü elektronik fatura                        |Avusturya         |
|Belçika'ya özgü elektronik fatura                         |Belçika         |
|NF-e Federal - Brezilya elektronik faturalama       |Brezilya          |
|NFS-e - Brezilya'ya özgü hizmet (şehir) elektronik fatura|Brezilya          |
|Danimarka'ya özgü elektronik fatura                          |Danimarka         |
|Mısır'a özgü elektronik fatura                        |Mısır           |
|Estonya'ya özgü elektronik fatura                        |Estonya         |
|Finlandiya'ya özgü elektronik fatura                         |Finlandiya         |
|Fransa'ya özgü elektronik fatura                          |Fransa          |
|Almanya'ya özgü elektronik fatura                          |Almanya         |
|PEPPOL - Küresel elektronik fatura                 |Genel          |
|İtalya'ya özgü elektronik fatura                         |İtalya           |
|CFDI - Meksika'ya özgü elektronik fatura                  |Meksika          |
|Hollanda'ya özgü elektronik fatura                           |Hollanda     |
|Norveç'e özgü elektronik fatura                       |Norveç          |
|İspanya'ya özgü elektronik fatura                         |İspanya           |

Ülke/bölge yerelleştirmeleri kapsamını destekleyen, eski bir elektronik faturalama özelliği olduğunda, bu Özelliklerden birinin etkinleştirilmesi eski özelliği devre dışı bırakır ve Elektronik faturalama ile Elektronik fatura kesmeyi etkinleştirir.

> [!IMPORTANT]
> Elektronik faturalama tümleştirme özelliği etkinleştirildikten sonra, yeni elektronik faturalama deneyimi varsayılan olarak kapalıdır. Özellik kavramını, ülkeye/bölgeye özel işlevleri kullanan yasal varlıklarla ilgili yeni deneyimleri seçerek etkinleştirmek için kullanabilirsiniz. **Genel** seçeneği, tabloda özel olarak listelenmeyen diğer ülke/bölgeler için yeni deneyimi denetler.

## <a name="submit-electronic-documents"></a>Elektronik belgeleri gönder

Elektronik belgeleri gönderme işlemi, Finance ve Supply Chain Management ile elektronik faturalama arasındaki tek iletişim noktasını temsil eder. Her gönderme olayı sırasında iletişim her iki yönde akar:

- **Finance ve Supply Chain Management'tan elektronik faturalamaya** – Finance ve Supply Chain Management, soyut faturaları Elektronik faturalamaya gönderir. Gerekirse, elektronik faturalama özelliklerinin bir parçası olarak konfigüre edilen değişkenlerin içeriğini de gönderir.
- **Elektronik faturalamadan Finance ve Supply Chain Management'a** - Elektronik faturalama özelliğine bağlı olarak, Supply Chain Management, daha önce gönderilen faturaların işleme sonuçları hakkında Elektronik faturalamadan güncelleştirmeleri alır. Elektronik faturalama özelliklerinin bir parçası olarak konfigüre edilen değişkenlerin içeriğini de alır.

Elektronik faturalama ile ilgili elektronik belgeleri göndermek için Finance ve Supply Chain Management'ta **Kuruluş yönetimi &gt; Periyodik &gt; Elektronik belgeler &gt; Elektronik belgeleri gönder**'e gidin.

Başlangıç noktası deftere nakledilen bir faturadır. Bu fatura; satış siparişleri, proje faturaları veya serbest metin faturaları gibi farklı kaynaklardan geliyor olabilir.

Gönderim süreci el ile veya arka planda çalıştırılabilir.

- **El ile yürütme** – El ile yürütme için, gönderilmesi gereken belge aralığını tanımlamak için **Filtre** seçeneğini kullanmalısınız. **Filtreler** sayfasında, gönderilmesi gereken deftere nakledilmiş faturaları seçmek için kendi sorgunuzu konfigüre edebilirsiniz. Seçim yapıldıktan sonra, işlemin yürütülmesini el ile başlatmanız ve çalışmasının bitmesini beklemeniz gerekir. İşlem tamamlandığında, İşlem merkezindeki bir ileti başarıyla gönderilen elektronik belge sayısını gösterir.
- **Arka planda yürütme** – Arka planda yürütme, oturum açmanız veya gönderme iletişim kutusunu açık tutmanız gerekmeden çalışır. İşlemi çalıştırmak ve çalıştırma sıklığını tanımlamak için zamanlayabilirsiniz.

## <a name="view-the-submission-logs"></a>Gönderme günlüklerini görüntüleme

Finance ve Supply Chain Management'ta, Elektronik faturalamaya gönderimin işlenmesinin sonuçlarını görmek için gönderme günlüklerini kullanabilirsiniz. **Kuruluş yönetimi &gt; Periyodik &gt; Elektronik belgeler &gt; Elektronik belge gönderimi**'ne gidin ve sonra **Belge türü** alanında, günlüklerin gösterdiği fatura türlerine filtre uygulamak için bir değer seçin.

Üç gönderme durumu vardır:

- **Planlandı** – Elektronik faturalama Finance ve Supply Chain Management'tan gönderilen gönderimi aldı ve elektronik faturalama özelliğinin işlemesi devam ediyor.
- **Tamamlandı** – Elektronik faturalama, elektronik faturalama özelliği kendisini çalıştırmak üzere yapılandırıldığı şekilde başarılı bir şekilde işlenmiştir.
- **Başarısız** – Elektronik faturalama bir hatayla karşılaştı veya elektronik faturalama özelliğinin işlenmesi sırasında bir özel durumla durduruldu.

> [!IMPORTANT]
> Gönderim durumu Elektronik faturalamanın elektronik faturalama özelliğinde yaptığı işlemin durumunu belirtir. Elektronik faturanın kendisinin nihai durumuna başvurmaz.
>
> Örneğin, bir elektronik faturanın onay için harici bir web hizmetine gönderilmesi gerekiyorsa gönderme durumu **Tamamlandı** olabilir ancak elektronik faturanın durumu **Reddedildi** olabilir. Bu durumda, Elektronik faturalama, elektronik faturalama özelliğini bu özelliği çalıştırmak üzere yapılandırıldığı şekilde başarılı bir şekilde işlemiştir. Ancak, elektronik fatura, web servisinin fatura onayı için belirlediği ölçütlere uygun olmadığı için reddedilmiştir.

Gönderme günlükleri aşağıdaki ek işlevleri içerir:

- **Gönderme ayrıntıları** – Ana gönderimin ayrıntılarını görüntüleyin. Görselleştirme, elektronik faturalama özelliğinde konfigüre edilen eylemlerin tam yürütme günlüğünü gösterir. Ayrıca, kullanıcıların işlem sırasında oluşturulan dosyaları indirmelerini sağlar. Faturanın harici bir web servisi tarafından onaylanması gereken senaryolarda, kullanıcıların faturanın durumunu görüntülemesine izin verir.
- **İlgili gönderiler** – Alt gönderimlerin ayrıntılarını görüntüleyin.
- **Gönderimleri iptal et** – Bu işlev, elektronik faturanın harici bir web servisi tarafından onaylanması gereken senaryolarda özel bir gönderme süreci yapılmasını sağlar. Elektronik faturalamanın, web servisi veritabanındaki onaylanmış bir elektronik faturanın durumunu iptal eden belirli bir ileti göndermesini sağlar.
- **Belgeyi yeniden gönder** – Elektronik faturalamanın zaten göndermiş olduğu elektronik belgeyi yeniden gönderin. **Gönderim ayrıntıları** sayfasında yeni bir günlük oluşturulur.
- **İlgili gönderimi gönder**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
