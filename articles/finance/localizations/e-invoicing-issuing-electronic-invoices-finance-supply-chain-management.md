---
title: Finance ve Supply Chain Management'ta elektronik fatura kesme
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında Elektronik faturalama eklentisi üzerinden nasıl elektronik fatura kesileceğini açıklamaktadır.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104449"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management'ta elektronik fatura kesme

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında Elektronik faturalama eklentisi üzerinden nasıl elektronik fatura kesileceğini açıklamaktadır.


## <a name="feature-activation"></a>Özellik etkinleştirme

Elektronik faturalama eklentisi ile elektronik faturalar kesmeye başlamak için, Finance ve Supply Chain Management'ta Özellik referansını etkinleştirmek gereklidir.

Her özellik referansı, bir ülke/bölge ile ilgili elektronik faturalama gereksinimlerini karşılayan belirli bir elektronik faturalama özelliğine karşılık gelir.

Aşağıdaki tabloda, elektronik faturalama eklentisinin desteklediği Özellik başvurularının listesi gösterilmektedir.

| Özellik referansı | Kuruluş adı                                              | Ülke/bölge |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e Federal - Brezilya elektronik faturalama       | Brezilya         |
| BR-00095          | NFS-e Brezilya elektronik faturaları               | Brezilya         |
| DK-00001          | Kamu sektörüne e-faturalama (OIOUBL) – DK    | Danimarka        |
| EG-00008          | Mısır için e-faturalama                             | Mısır          |
| ES-00025          | Kamu sektörüne elektronik fatura           | İspanya          |
| EUR-00023         | Avrupa Birliği Kamu sektörüne e-fatura kesme       | Avrupa         |
| ITA-00036         | IT - Kamu sektörüne elektronik E-Fatura (FatturaPA) | İtalya          |
| MX-00010          | E-faturalama CFDI                                  | Meksika         |
| MX-00016          | E-faturalama CFDI - iptal işlemi           | Meksika         |

Ülke yerelleştirmeleri kapsamını destekleyen, eski bir elektronik faturalama özelliği olduğu durumlarda, Özellik başvurusunun etkinleştirilmesi Elektronik faturalama eklentisi ve önceki özelliğin devre dışı bırakma işlemlerinde Elektronik fatura kesmeyi etkinleştirir.

## <a name="submit-electronic-documents"></a>Elektronik belgeleri gönder

Elektronik belgeleri gönderme işlemi, Finance ve Supply Chain Management ile elektronik faturalama eklentisi arasındaki tek iletişim noktasını temsil eder. Her gönderme olayı sırasında iletişim her iki yönde akar:

- **Finance ve Supply Chain Management'tan elektronik faturalama eklentisine** – Finance ve Supply Chain Management, soyut faturaları Elektronik faturalama eklentisine gönderir. Gerekirse, elektronik faturalama özelliklerinin bir parçası olarak konfigüre edilen değişkenlerin içeriğini de gönderir.
- **Elektronik faturalama eklentisinden Finance ve Supply Chain Management'a** - Elektronik faturalama özelliğine bağlı olarak, Supply Chain Management, daha önce gönderilen faturaların işleme sonuçları hakkında Elektronik faturalama eklentisinden güncelleştirmeleri alır. Elektronik faturalama özelliklerinin bir parçası olarak konfigüre edilen değişkenlerin içeriğini de alır.

Elektronik faturalama eklentisi ile ilgili elektronik belgeleri göndermek için Finance ve Supply Chain Management'ta **Kuruluş yönetimi &gt; Periyodik &gt; Elektronik belgeler &gt; Elektronik belgeleri gönder**'e gidin.

Başlangıç noktası deftere nakledilen bir faturadır. Bu fatura; satış siparişleri, proje faturaları veya serbest metin faturaları gibi farklı kaynaklardan geliyor olabilir.

Gönderim süreci el ile veya arka planda çalıştırılabilir.

- **El ile yürütme** – El ile yürütme için, gönderilmesi gereken belge aralığını tanımlamak için **Filtre** seçeneğini kullanmalısınız. **Filtreler** sayfasında, gönderilmesi gereken deftere nakledilmiş faturaları seçmek için kendi sorgunuzu konfigüre edebilirsiniz. Seçim yapıldıktan sonra, işlemin yürütülmesini el ile başlatmanız ve çalışmasının bitmesini beklemeniz gerekir. İşlem tamamlandığında, İşlem merkezindeki bir ileti başarıyla gönderilen elektronik belge sayısını gösterir.
- **Arka planda yürütme** – Arka planda yürütme, oturum açmanız veya gönderme iletişim kutusunu açık tutmanız gerekmeden çalışır. İşlemi çalıştırmak ve çalıştırma sıklığını tanımlamak için zamanlayabilirsiniz.

## <a name="view-the-submission-logs"></a>Gönderme günlüklerini görüntüleme

Finance ve Supply Chain Management'ta, Elektronik faturalama eklentisine gönderimin işlenmesinin sonuçlarını görmek için gönderme günlüklerini kullanabilirsiniz. **Kuruluş yönetimi &gt; Periyodik &gt; Elektronik belgeler &gt; Elektronik belge gönderimi**'ne gidin ve sonra **Belge türü** alanında, günlüklerin gösterdiği fatura türlerine filtre uygulamak için bir değer seçin.

Üç gönderme durumu vardır:

- **Planlandı** – Elektronik faturalama eklentisi Finance ve Supply Chain Management'tan gönderilen gönderimi aldı ve elektronik faturalama özelliğinin işlemesi devam ediyor.
- **Tamamlandı** – Elektronik faturalama eklentisi, elektronik faturalama özelliği kendisini çalıştırmak üzere yapılandırıldığı şekilde başarılı bir şekilde işlenmiştir.
- **Başarısız** – Elektronik faturalama eklentisi bir hatayla karşılaştı veya elektronik faturalama özelliğinin işlenmesi sırasında bir özel durumla durduruldu.

> [!IMPORTANT]
> Gönderim durumu Elektronik faturalama eklentisinin elektronik faturalama özelliğinde yaptığı işlemin durumunu belirtir. Elektronik faturanın kendisinin nihai durumuna başvurmaz.
>
> Örneğin, bir elektronik faturanın onay için harici bir web hizmetine gönderilmesi gerekiyorsa gönderme durumu **Tamamlandı** olabilir ancak elektronik faturanın durumu **Reddedildi** olabilir. Bu durumda, Elektronik faturalama eklentisi, elektronik faturalama özelliğini bu özelliği çalıştırmak üzere yapılandırıldığı şekilde başarılı bir şekilde işlemiştir. Ancak, elektronik fatura, web servisinin fatura onayı için belirlediği ölçütlere uygun olmadığı için reddedilmiştir.

Gönderme günlükleri aşağıdaki ek işlevleri içerir:

- **Gönderme ayrıntıları** – Ana gönderimin ayrıntılarını görüntüleyin. Görselleştirme, elektronik faturalama özelliğinde konfigüre edilen eylemlerin tam yürütme günlüğünü gösterir. Ayrıca, kullanıcıların işlem sırasında oluşturulan dosyaları indirmelerini sağlar. Faturanın harici bir web servisi tarafından onaylanması gereken senaryolarda, kullanıcıların faturanın durumunu görüntülemesine izin verir.
- **İlgili gönderiler** – Alt gönderimlerin ayrıntılarını görüntüleyin.
- **Gönderimleri iptal et** – Bu işlev, elektronik faturanın harici bir web servisi tarafından onaylanması gereken senaryolarda özel bir gönderme süreci yapılmasını sağlar. Elektronik faturalama eklentisinin, web servisi veritabanındaki onaylanmış bir elektronik faturanın durumunu iptal eden belirli bir ileti göndermesini sağlar.
- **Belgeyi yeniden gönder** – Elektronik faturalama eklentisinin zaten göndermiş olduğu elektronik belgeyi yeniden gönderin. **Gönderim ayrıntıları** sayfasında yeni bir tam günlük oluşturulur.
- **İlgili gönderimi gönder**
