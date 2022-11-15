---
title: Yıl sonu kapanışını optimize etme
description: Bu makalede, genel muhasebe yıl sonu kapanış işlemi için kullanılan Yıl sonu kapanışını optimize etme hizmet eklentisi açıklanmaktadır.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750019"
---
# <a name="optimize-year-end-close"></a>Yıl sonu kapanışını optimize etme

Microsoft Dynamics 365 Finance için Yıl sonu kapanışını optimize etme hizmet eklentisi, Dynamics 365 Finance kaynakları için Uygulama Nesne Sunucusu (AOS) kurulumunun dışında çalıştırılacak yıl sonu kapanışı işlemini etkinleştirir. Mikro hizmet teknolojisini kullanır. Yıl sonu kapanışını optimize etme işleviyle ilişkili kazançlar arasında yıl sonu kapanışı işlemi sırasında artan performans ve SQL veritabanı üzerinde en az etki vardır.

Yıl sonu kapanışını optimize etme işlevini kullanmak için aşağıdaki görevleri tamamlamanız gerekir:

1. Microsoft Dynamics Lifecycle Service'teki projenizden yıl sonu kapanışını optimize etme hizmet eklentisini yükleyin.
2. Özellik yönetiminde **Yıl sonu kapanışını optimize etme** özelliğini etkinleştirin.

> [!NOTE]
> Özellik yönetiminde **Yıl sonu kapanışını optimize etme** özelliğini devre dışı bırakarak Finans kaynakları için geçerli yıl sonu kapanışı işlevini kullanmaya devam edebilirsiniz.

## <a name="improved-performance"></a>Artan performans

**Yıl sonu kapanışını optimize etme** özelliği, özellikle büyük miktarda veriye sahip müşterilerin yıl sonu kapanışı işlemlerini hızlandırmak için tasarlanmıştır. Yıl sonu kapanışı bir hizmette çalıştığında yoğun işlemler, işlem süresinin azaltılmasına ve diğer kullanıcıların günlük işlemlerini etkileyebilecek kaynakların serbest bırakılmasına yardımcı olmak için Finans kaynaklarından aktarılır.

**Yıl sonu kapanışını optimize etme** özelliği, aşağıdaki hedeflere ulaşmada size yardımcı olabilir:

- Çalışma zamanını azaltarak yıl sonu kapanışı performansını iyileştirin.
- Yıl sonu kapanışının çalışması sırasında diğer süreçler üzerindeki etkiyi azaltın.
- Yıl sonu kapanışı çalıştırması daha az zaman aldığından yıl sonu sonuçları için raporlama ve ayarlamaları iyileştirin.

## <a name="new-options-and-visibility"></a>Yeni seçenekler ve görünürlük

**Yıl sonu kapanışını optimize et** özelliği etkinleştirildiğinde aşağıdaki yerlere **Sonuçlar** ve **Durum** olmak üzere iki yeni sütun eklenir:

- **Yıl sonu kapanışı** sayfasına
- **Yıl sonu kapanışı sonuçları** iletişim kutusuna
- **Yıl sonu kapanışı şablonu** sayfasının **Bilanço mali boyut transferi** seçeneklerine

Aşağıdaki şekilde **Yıl sonu kapanışı** sayfasındaki **Sonuçlar** ve **Durum** sütunlarının bir örneği gösterilmektedir. Yıl sonu kapanışının sonuçlarını açmak için **Sonuçlar** sütunundaki **Sonuçları görüntüle** bağlantısını seçebilirsiniz. **Durum** sütunu, yıl sonu kapanışı işleminin geçerli durumunu gösterir. Bu nedenle, yeni sütunlar yıl sonu kapanışı işleminin ilerlemesiyle ilgili görünürlük sağlar.

[![Yıl sonu kapanışı sayfasındaki Sonuçlar ve Durum sütunları.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Ayrıca **Yıl sonu kapanışını optimize etme** özelliği etkinleştirildiğinde **Yıl sonu kapanışı şablonu** sayfasında **Bilanço mali boyutları** hızlı sekmesi kullanılabilir hale gelir. Bir yılı kapatırken bilanço mali boyutlarını ayrıntılı olarak belirtmek için bu hızlı sekmeyi kullanabilirsiniz. Bu özellik, kar ve zarar hesapları için şu anda sunulan özelliği paraleldir.

## <a name="architecture-and-data-flow"></a>Mimari ve veri akışı

Bir mikro hizmette **Yıl sonu kapanışını optimize etme** özelliğini kullanmak ve yıl sonu kapanışını çalıştırmak için Lifecycle Services'ten Yıl sonu kapanışını optimize etme hizmet eklentisini yüklemeniz ve ardından Özellik yönetiminde **Yıl sonu kapanışını optimize etme** özelliğini etkinleştirmeniz gerekir.

Aşağıdaki şekilde gösterildiği gibi yıl sonu kapanışı işlemi, eklentinin yüklendiğini ve özelliğin etkinleştirildiğini doğrular. Her iki ön koşul da karşılanırsa yıl sonu kapanışı mikro hizmette çalışır.

[![Veri akışı diyagramı.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Yıl sonu kapanışı işlemi için üst düzey akış

1. Yıl sonu kapanışı işlemi Finance'de **Genel muhasebe \> Dönem kapanışı \> Yıl sonu kapanışı** bölümünde başlatılır. İşlem, kapatılan tüzel kişilikler için kapanış toplu işleri ve görevleri oluşturur.
2. Yıl sonu kapanışı, yıl sonu kapanışının mikro hizmette mi yoksa geçerli kapanış mantığında mı çalıştırılacağını belirler.

    - Lifecycle Services'te Yıl sonu kapanışını optimize etme hizmeti eklentisi yüklüyse ve Özellik yönetiminde **Yıl sonu kapanışını optimize etme** özelliği etkinleştirilirse yıl sonu kapanışı mikro hizmette çalışır.

        1. Yıl sonu kapanışını optimize etme işlevi, kapatılan her tüzel kişilik için bir yıl sonu kapanış hizmeti işi oluşturur ve ardından yıl sonu kapanışı mantığını çalıştırır. Mikro hizmet yıl sonu kapanışını gerçekleştirir.
        2. Finance, mikro hizmetin ne zaman tamamlandığını belirlemek için mikro hizmette yıl sonu kapanışını dinler. Ardından yıl sonu kapanışı sonuçları Finance'de **Yıl sonu kapanışı** sayfasında güncelleştirilir.

    - Aksi takdirde yıl sonu kapanışı geçerli kapanış mantığında çalışır.
