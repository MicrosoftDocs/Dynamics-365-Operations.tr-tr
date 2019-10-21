---
title: Bakım tahminleri
description: Bu konuda Varlık Yönetimi'nde bakım tahminleri açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024511"
---
# <a name="maintenance-forecasts"></a>Bakım tahminleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Bir iş emri oluşturduğunuzda, ilgili varlıklar ve bakım işi türleriyle iş emri işleri oluşturursunuz. Bakım tahminlerini içeren bir bakım işi türü seçtiğinizde, tahminler otomatik olarak iş emrine kopyalanır.

Bir iş emrinde tahmin satırları ekleyebilir veya silebilirsiniz. Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje tipiyle ilgili aşama kuralları kurulumu, tahmin satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler. 

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. Listeden iş emrini seçin ve **Tahmin**'e tıklatın. **İş emri bakım tahmininde**, iş emri işinde seçilen bakım işi türünden gelen tahmin satırları görüntülenir.


## <a name="add-hours-forecast-to-a-work-order"></a>İş emrine tahmin saatleri ekleme

1. Tahmin eklemek istediğiniz iş emri işini seçin.

2. **Saatler** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'ye tıklayın.

3. **Kategori** alanında bir kategori seçin.

4. **Saat** alanına tahmini saat sayısı ekleyin.

5. **Satır özelliği** alanında, satırda kullanılacak masraf türünü seçin.


## <a name="add-items-forecast-to-a-work-order"></a>İş emrine madde tahminleri ekleme

Bir iş emri bakım tahminine madde eklemenin üç yolu vardır: Yedek parça listesi veya varlık ürün reçetesine dahil edilmeyen maddeler (yedek parçalar) için satırlar oluşturabilir, onaylanan yedek parçalar listesinden yedek parçalar seçebilir ve maddeleri Varlık ürün reçetesinden seçebilirsiniz.

1. Tahmin eklemek istediğiniz iş emri işini seçin.

2. **Maddeler** hızlı sekmesini seçin.

3. Yedek parçalar listesi veya varlık ürün reçetesi listesinde bulunmayan bir yedek parça için yeni bir satır oluşturmak üzere **Ekle**'yi tıklatın.

4. **Madde numarası** alanında bir maddeyi seçin.

5. **Satış miktarı** alanına miktar ekleyin ve **Birim** alanında bir miktar birimi seçin.

6. İlgili alanlara maliyet fiyatını ve para birimini ekleyin ve bir **Satır özelliği** seçin.

7. Madde satırlarında görüntülenen boyutların listesini değiştirmek isterseniz **Stok** > **Boyutları görüntüle**'ye tıklayın, boyutları seçin ve **Kurulumu kaydet** düğmesinde "Evet" seçeneğini belirleyin.

8. Bakım tahminine onaylı bir yedek parça eklemek istiyorsanız, **Yedek parça ekle**'ye tıklayın, yedek parçayı seçin, gerekiyorsa ilgili bilgileri düzenleyin **Tamam**'a tıklayın.

9. Tahmine varlık ürün reçetesi maddeleri eklemek istiyorsanız, **Ürün reçetesi maddeleri ekle**'ye tıklatın, maddeyi seçin, gerekiyorsa ilgili bilgileri düzenleyin ve **Tamam**'ı tıklatın.

10. Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım iş türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. 



## <a name="add-expense-forecast-to-a-work-order"></a>İş emrine gider tahminleri ekleme

1. Bu konu, bir iş emrine nasıl gider tahmini ekleneceğini açıklamaktadır. Formun sol tarafında, tahmin eklemek istediğiniz iş emri işini seçin.

2. **Gider** hızlı sekmesini seçin.

3. Yeni bir satır oluşturmak için **Ekle**'ye tıklayın.

4. **Kategori** alanında bir kategori seçin.

5. **Miktar** alanına miktarı girin.

6. İlgili alanlara maliyet fiyatı, satış para birimi ve satış fiyatını ekleyin.

7. **Satır özelliği** alanında, satırda kullanılacak masraf türünü seçin.

>[!NOTE]
>**Bakım tahmini toplamları** hızlı sekmesinde, seçili iş emri işi ve iş emri için her bir sekmede oluşturulan satır sayısının genel görünümünü görebilirsiniz. Ayrıca, iş emri işi ve iş emri için tahmin edilen çalışma saatlerinin toplamını görebilirsiniz.

![Şekil 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>İş emri tahminlerini otomatik güncelleştirme

Varlık Yönetimi'nde, diğer modüllerde güncelleştirilen saat maliyetleri, madde maliyetleri ve giderler için iş emri tahminlerindeki değişiklikleri otomatik olarak güncelleştirebilirsiniz. Bu işlem, en son maliyet fiyatlarının iş emri tahminlerinde her zaman kullanılmasını sağlamak için yapılır. [Bakım işi türü tahminlerinde](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) de benzer güncelleştirmeler yapmak mümkündür.

1. **Varlık yönetimi** > **Periyodik** > **Tahmin** > **İş emri tahmini güncelleştir** seçeneğine tıklayın.

2. **İş emri tahminini güncelleştir** iletişim kutusunda gerekirse, belirli iş emirleri veya iş emri işleriyle ilgili seçimler ekleyebilirsiniz. Bu seçimleri yapmak için **Filtre**'ye tıklayın.

3. Gerekirse, **Arka planda çalıştır** hızlı sekmesinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.

4. Tahmin güncelleştirmesini başlatmak için **Tamam**'a tıklayın.


![Şekil 2](media/07-work-orders.png)

