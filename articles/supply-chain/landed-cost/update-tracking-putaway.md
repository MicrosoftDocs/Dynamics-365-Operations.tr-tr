---
title: Yerine koyma için izlemeyi güncelleme
description: Bu makalede, Yerine koyma için izlemeyi güncelleştirme periyodik görevinin nasıl kurulacağı ve çalıştırılacağı açıklanmaktadır.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b36fe5a9828ea018881f08b8af27d77cdf0babc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882619"
---
# <a name="update-tracking-for-put-away"></a>Yerine koyma için izlemeyi güncelleştirme

[!include [banner](../includes/banner.md)]

*Yerine koyma için izlemeyi güncelleştir* periyodik görevi, her gece yinelenen bir toplu iş olarak çalıştırılmak üzere tasarlanmıştır. Hangi seferlerin tüm stok hareketlerini aldığını ve hangi seferlerin fiili bitiş tarihi için bir değeri olmadığını tanımlar. Ardından, fiili bitiş tarihini gerektiği şekilde geçerli tarihe ayarlar.

*Sevkiyat konteynerleri*'nin tüm yolculuklarının her bir *aşaması* için *konteyner etkinlikleri* oluşturulur. Bu değerler, bir yolculuk oluşturulduğunda seçilen yolculuk şablonu tarafından tanımlanır. Her bir konteyner etkinliği kaydı için **Başlangıç tarihi**, **Tahmini bitiş tarihi** ve **Fiili bitiş tarihi** alanlarına değerler ayarlanabilir. Bu alanlar, bir aşamanın başladığına veya tamamlandığına dair onay alındığında güncelleştirilebilir.

Genellikle, bu eylemler Microsoft Dynamics 365 Supply Chain Management uygulamasının dışında tutulduğundan onaylanan tarihlerle ilgili bilgiler, nakliye aracısı gibi bir üçüncü taraf aracılığıyla sağlanır. Ancak malların bir yolculuk aşamasından ambara gelişini izlemek için üçüncü taraf aracılığıyla sağlanan bilgi gerekli değildir (malların yerine konmasıyla işaretlenmesi gibi). Bu nedenle izleme, Dynamics 365 Supply Chain Management uygulamasındaki bilgiler temel alınarak belirlenebilir.

*Yerine koyma için izlemeyi güncelleştir* periyodik görevini kurmak ve çalıştırmak için şu adımları izleyin:

1. **Son Teslim Alma Maliyeti \> Periyodik görevler \> Yerine koyma için izlemeyi güncelleştir**'e gidin.
1. **Yerine koyma için izlemeyi güncelleştir** iletişim kutusundaki **Parametreler** bölümünde aşağıdaki alanları ayarlayın:

    - **Aşama**: Bir yolculuğun izlenmesini güncelleştirmek istediğiniz bölümü için benzersiz kimlik adını/numarasını seçin. Seçilen değer, seferin ambara varışını temsil etmelidir.
    - **Etkinlik**: Seçilen aşama sırasında gerçekleştirilen etkinliği seçin. Bu değerler, izleme denetim merkezindeki yolculuk şablonu satırı başına atanır.

1. Güncelleştirmeye dahil edilmesi gereken kayıt kümesini sınırlamak için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele** düğmesini seçin. Seçim ölçütünü, sıralama ölçütünü ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Supply Chain Management'ta bulunan diğer sorgular için çalıştıkları gibi çalışır. Buradaki alanlar salt okunurdur ve sorgunuzla ilgili değerleri gösterir.
1. **Arka planda çalıştır** hızlı sekmesinde, Supply Chain Management'taki diğer iş türleri için yapacağınız şekilde, ihtiyaç duyduğunuz toplu iş ve zamanlama seçeneklerini ayarlayın.
1. Ayarlarınızı uygulamak ve güncelleştirmeyi çalıştırmak veya zamanlamak için **Tamam**'ı seçin.
