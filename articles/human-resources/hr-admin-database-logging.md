---
title: Veritabanı günlüğü yapılandırma ve yönetme
description: Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129291"
---
# <a name="configure-and-manage-database-logging"></a>Veritabanı günlüğü yapılandırma ve yönetme

Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz. Bu konuda, aşağıdakilerin nasıl yapılacağı açıklanmaktadır:

- Veritabanı günlükleri için güvenlik ve performansı yönetme
- Veritabanı günlüğe kayıt ayarla
- Veritabanı günlüklerini temizleme

## <a name="overview-of-database-logging"></a>Veritabanı günlüklerine genel bakış

Veritabanı günlükleri Microsoft Dynamics 365 Human Resources'taki tablo ve alanlarda yapılan belirli değişiklikleri izler. Bu değişiklikler ekleme, güncelleştirme veya silmeyi içerir. Veritabanı günlükleri, veritabanı günlüğü tablosundaki tablo veya alanlardaki değişikliklerin kaydını depolar.

Veritabanı günlüğünün iş için kullanımı şunları içerir:

- Hassas bilgiler içeren belirli tablolardaki değişikliklerin denetim kaydını oluşturmak.
- Tek hareketleri izlemek. Veritabanı günlükleri toplu işlemlerde çalışan otomatik hareketleri izlemek için tasarlanmamıştır.

## <a name="security-for-database-logging"></a>Veritabanı günlükleri için güvenlik

Veritabanı günlükleri hassas veriler içerebilir. Erişimi yalnızca günlük verisine erişmesi gereken güvenlik rollerini içerecek şekilde sınırlayın.

## <a name="database-logging-and-performance"></a>Veritabanı günlüğü ve performansı

İş açısından bakıldığında çok değerli olmasına karşın, veritabanı günlükleri kaynak kullanımı ve yönetimi açısından pahalı olabilir. Veritabanı günlüğünün performans etkileri şunları içerir:

- Veritabanı günlüğü tablosu hızlı bir şekilde büyüyebilir ve veritabanı boyutunun artmasına neden olabilir. Büyüme, korumak istediğiniz günlüğe kaydedilmiş veri miktarına bağlıdır. Varsayılan olarak, veritabanı günlüğü tablosu yalnızca 30 günlük verilerini korur. 

- Veritabanı günlükleri uzun süre çalışan veri içe aktarma işlemleri gibi uzun süren otomatikleştirilmiş işlemleri olumsuz etkileyebilir.

### <a name="best-practices"></a>Önerilen yöntemler

Performansı artırmak için, tabloların tamamı yerine günlüğe kaydedilecek belirli alanları seçerek günlük girişlerini sınırlayın. Genel performansın sürdürülmesine yardımcı olmak için, veritabanı günlüğü kaydı 20 tabloyla sınırlıdır.

> [!NOTE]
> Tek tek alanlar için yalnızca güncelleştirmeler günlüğe kaydedilebilir.

## <a name="set-up-database-logging"></a>Veritabanı günlüğe kayıt ayarla

Veritabanı günlüğü kaydını ayarlamak için **Veritabanı değişikliklerini günlüğe kaydetme** sihirbazını kullanabilirsiniz. Sihirbaz, tablolar veya alanların günlüğe kaydedilmesini ayarlamak için esnek bir yol sağlar.

1. **Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri kurulumu**'na gidin. **Veri tabanı değişikliklerini günlüğe kaydetme** sihirbazında **Yeni**'yi seçin.
2. Sihirbazı tamamlayın.

## <a name="clean-up-database-logs"></a>Veritabanı günlüklerini temizleme

Veritabanı günlüklerinin tümünü veya bir bölümünü aşağıdaki seçenekleri kullanarak silebilirsiniz:

- Belirli bir tabloya ait tüm günlükleri seçin.
- Belirli veritabanı günlüğü türlerini seçin.
- Günlüğün oluşturulduğu tarih ve saati seçin.

Veritabanı günlüğü temizleme işlemi ayarlamak için aşağıdaki adımları izleyin: 

1. **Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri**'ne gidin. **Günlüğü temizle**'yi seçin.

2. Aşağıdaki seçeneklerden birini girerek, günlükleri silmek üzere seçebileceğiniz bir yöntem seçin:

   - Tablo ID
   - Günlük türü
   - Oluşturma tarihi ve saati

3. Günlük temizleme görevinin ne zaman çalıştırılacağını belirlemek için **Veritabanı günlüklerini temizleme** sekmesini kullanın. Varsayılan olarak, veritabanı günlükleri 30 gün süreyle kullanılabilir.
