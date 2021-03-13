---
title: Bakım tahminleri
description: Bu konuda Varlık Yönetimi'nde bakım tahminleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c60834a1f818b142a0f2f022d66fe1f42edeb536
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020884"
---
# <a name="maintenance-forecasts"></a>Bakım tahminleri

[!include [banner](../../includes/banner.md)]



Bir iş emri oluşturduğunuzda, ilgili varlıklar ve bakım işi türleri bulunan iş emri işleri oluşturursunuz. Bakım tahminlerini içeren bir bakım işi türü seçtiğinizde, tahminler otomatik olarak iş emrine kopyalanır.

Bir iş emrine tahmin satırları ekleyebilir veya bunları bir iş emrinden silebilirsiniz. Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje türüyle ilgili aşama kuralları kurulumu, tahmin satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler. İş emri yaşam döngüsü durumları ve ilgili proje aşamaları hakkında daha fazla bilgi için bkz. [Tahminler, iş emirleri ve projeler](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. Listede iş emrini seçin ve sonra Eylem bölmesinde > **İş emri** sekmesinde > **Proje** grubunda **Tahmin** öğesini seçin. **İş emri bakım tahmini** sayfasında, iş emri işinde seçilen bakım işi türünden gelen tahmin satırları görüntülenir.


## <a name="add-an-hours-forecast-to-a-work-order"></a>İş emrine saat tahmini ekleme

1. **İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.

2. **Saatler** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'yi seçin.

3. **Kategori** alanında bir kategori seçin.

4. **Saat** alanına tahmini saat sayısını girin.

5. **Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.


## <a name="add-an-items-forecast-to-a-work-order"></a>İş emrine madde tahmini ekleme

Bir iş emri bakım tahminine madde eklemenin üç yolu vardır. Yedek parça listesi veya varlık ürün reçetesine (BOM) dahil edilmeyen maddeler (yedek parçalar) için satırlar oluşturabilir, onaylanan yedek parçalar listesinden yedek parçalar seçebilir veya maddeleri Varlık ürün reçetesinden seçebilirsiniz.

- **İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.

- **Maddeler** hızlı sekmesinde, uygun yöntemi kullanarak bakım tahminine maddeler ekleyin.

Yedek parçalar listesi veya varlık ürün reçetesinde bulunmayan bir yedek parça için yeni bir satır oluşturmak üzere şu adımları izleyin.

1. **Ekle**'yi seçin.
2. **Madde numarası** alanında maddeyi seçin.
3. **Satış miktarı** alanına miktarı girin.
4. **Birim** alanında, miktar için ölçü birimini seçin.
5. **Maliyet fiyatı** ve **Para birimi** alanlarına ilgili değerleri girin.
6. **Satır özelliği** alanında bir satır özelliği seçin.
7. Madde satırlarında görüntülenen boyutların listesini değiştirmek için **Stok** > **Boyutları görüntüle**'yi seçin, boyutları seçin ve ardından **Kurulumu kaydet** seçeneğini **Evet** olarak ayarlayın.

Onaylı bir yedek parça listesinden yedek parça eklemek için şu adımları izleyin:

1. **Yedek parça ekle**'yi seçin.
2. Yedek parçayı seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.
3. **Tamam**'ı seçin.

Varlık ürün reçetesinden bir madde eklemek için şu adımları izleyin:

1. **Ürün reçetesi maddeleri ekle**'yi seçin.
2. Maddeyi seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.
3. **Tamam**'ı seçin.

Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım işi türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. Bu genel bakış hakkında daha fazla bilgi için bkz. [Maddenin kullanıldığı yer](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>İş emrine gider tahmini ekleme

1. **İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.

2. **Gider** hızlı sekmesinde satır oluşturmak için **Ekle**'yi seçin.

3. **Kategori** alanında bir kategori seçin.

4. **Miktar** alanına miktarı girin.

5. **Maliyet fiyatı**, **Satış para birimi** ve **Satış fiyatı** alanlarına uygun değerleri girin.

6. **Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.

>[!NOTE]
>**Bakım tahmini toplamları** hızlı sekmesi, seçili iş emri işi ve iş emri için her hızlı sekmede oluşturulan satır sayısının genel görünümünü gösterir. Ayrıca, iş emri işi ve iş emri için tahmin edilen çalışma saatlerinin toplamını da gösterir.

Aşağıdaki şekilde **İş emri bakım bakım tahmini** sayfası örneği gösterilmektedir.

![Şekil 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>İş emri tahminlerini otomatik güncelleştirme

Microsoft Dynamics 365 for Finance and Operations'daki diğer modüllerde saat maliyetleri, madde maliyetleri ve giderler güncelleştirilirse Varlık Yönetimindeki iş emri tahminleri bu değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilebilir. Bu özellik, en son maliyet fiyatlarının iş emri tahminlerinde her zaman kullanılmasını sağlamaya yardımcı olur. [Bakım işi türü tahminlerinde](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) de benzer güncelleştirmeler yapabilirsiniz.

1. **Varlık yönetimi** > **Periyodik** > **Tahmin** > **İş emri tahminini güncelleştir**'i seçin.

2. **İş emri tahminini güncelleştir** iletişim kutusunda, **Dahil edilecek kayıtlar** hızlı sekmesinde gerekirse, belirli iş emirleri veya iş emri işleriyle ilgili seçimler ekleyebilirsiniz. İlgili seçimleri yapmak için **Filtre**'yi seçin.

3. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.

4. Tahmin güncelleştirmesini başlatmak için **Tamam**'ı seçin.


Aşağıdaki şekilde **İş emri tahmini güncelleştir** iletişim kutusu örneği gösterilmektedir.

![Şekil 2](media/07-work-orders.png)
