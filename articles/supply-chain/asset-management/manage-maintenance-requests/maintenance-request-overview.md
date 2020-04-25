---
title: Bakım talepleri
description: Bu konu, varlık yönetimi'nde bakım taleplerini yönetme hakkında genel bir bakış sağlar
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c911f1a0cd895899f85ae8f5ec4c3fcc847c0cf0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205173"
---
# <a name="maintenance-requests"></a>Bakım talepleri

[!include [banner](../../includes/banner.md)]

 

Bakım talepleri, bir varlığın bir bakım veya onarım işi gerektirebileceği ancak bir iş emri oluşturmadan yöneticiye veya planlayıcıya bildirmek için oluşturulan notlar veya beyanlardır. Bakım talebinin içeriği geçerli kabul edilir, bir iş emri daha sonra bakım talebine göre oluşturulabilir.

Bakım talepleri, Varlık yönetimi'ndeki herhangi bir varlık için oluşturulabilir. Şirketinizin bakım taleplerini nasıl kullandığına bağlı olarak çeşitli bakım talepleri oluşturulabilir. Burada bazı örnekler verilmiştir:

- Bakım talepleri
- Notlar
- Düzeltmeler ya da yükseltmeler
- Yatırımlar
- Depo onarımı (Bu tür, bir bakım veya onarım işi yapmak ve iş tamamlandıktan sonra varlığı geri dönmek için başka bir konumdan varlıklar aldığınızda kullanılır.)

## <a name="view-maintenance-requests"></a>Bakım taleplerini görüntüle

Bakım taleplerini görüntülemek için **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri**, **Etkin bakım talepleri**, ya da **İşlem yapılacak yerleşim bakım talepleri**'ni seçin. Her liste sayfası bir bakım talebi ile ilgili bazı bilgileri gösterir.

![Bakım taleplerini görüntüle](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Çalışan olarak ilişkili olduğunuz işlem yapılacak yerleşimleri veya ilişkili olduğunuz işlem yapılacak yerleşimlere yüklü varlıkları içeren bakım taleplerinin listesini görüntülemek için **İşlem yapılacak yerleşim bakım talepleri** liste sayfasını kullanın. (Bakım çalışanlarında işlem yapılacak yerleri ayarlama hakkında daha fazla bilgi için bkz: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Müşteri hesabı bilgileri Varlık hizmeti yönetimi'nde (dış bakım) kullanılabilir olsa da, Varlık yönetimi'nde (iç bakım) kullanılamaz.

Bir kaydın Ayrıntılar görünümünü açmak için, **Tüm bakım talepleri** listesi sayfasında, kılavuz görünümünde, **Bakım talebi** sütununda bir bağlantı seçin.

![Bakım talebi ayrıntılarını görüntüleme](media/02-manage-maintenance-requests.png)

Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir. Aşağıdaki tabloda Kıymet Yönetimi'yle ilgili düğmeler kısaca açıklanmaktadır.

| Düğme adı                      | Tanım |
|----------------------------------|-------------|
| Düzenle                             | Seçili bakım talebini düzenleyin. |
| Yeni                              | Yeni bakım talebi oluşturun. |
| Sil                           | Seçili bakım talebini silin. |
| İş emri havuzu                  | Seçili bakım talebini bir iş emri havuzuna bağlayın. |
| İş emri                       | Seçili bakım talebine bağlı olarak bir iş emri oluşturun. |
| Varlık hatası                      | Seçili bakım talebine hata kaydı oluşturabileceğiniz **varlık hataları**'na tıklayın. |
| İş emirleri                      | Seçili bakım talebine bağlı olan tüm iş siparişlerinin bir listesini göster. |
| Bakım talebi durumunu güncelleştir | Bakım talebi durumunu güncelleştirin. |
| Yaşam döngüsü durumu günlüğü              | Seçili bakım talebinin yaşam döngüsü durumlarını gösteren günlüğü görüntüleyin. |
| Bakım talebi ayrıntıları      | Seçili bakım talebinin ayrıntılarını gösteren bir rapor yazdırın. |
| Ödünç varlığı gönder                  | Seçili bakım talebinde seçilen varlığın geçici olarak değiştirilmesi gereken bir kredi varlığı seçin. |
| Kredi varlıklarını iade etme                | İade edilen ödünç varlığını kaydedin. |

