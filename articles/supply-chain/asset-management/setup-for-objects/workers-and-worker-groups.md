---
title: Bakım görevlileri ve çalışan grupları
description: Bu konuda Kıymet Yönetimi'nde bakım görevlileri ve çalışan grupları açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b81de02f144712786704a46d2096dfb510d5ce68
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017404"
---
# <a name="maintenance-workers-and-worker-groups"></a>Bakım görevlileri ve çalışan grupları

[!include [banner](../../includes/banner.md)]

 

Bu konuda Kıymet Yönetimi'nde bakım görevlileri ve çalışan grupları açıklanmaktadır. Kıymet Yönetimi'nde bakım çalışanlarını işlem yapılacak yerleşimlerle bağlayabilirsiniz. (İşlem yapılacak yerleşimler hakkında daha fazla bilgi için bkz. [İşlem yapılacak yerleşimleri oluşturma](../functional-locations/create-functional-locations.md).) Bu işlev işlem yapılacak yerleşim 01'de bulunan bir makinede bakım işi zamanlarken ve işi gerçekleştirmesi için aynı konumdan bakım görevlilerini tahsis etmek istediğinizde yararlı olabilir.

Ayrıca bakım görevlisi grupları oluşturabilir ve bakım görevlilerini bu gruplarla ilişkilendirebilirsiniz. Bu işlev basit bir iş emri planlaması yaparken ve bir iş emrinde bakım görevlileri grubunu planlamak istediğinizde yararlıdır. Bakım görevlilerini ve bakım görevlisi gruplarını tercih edilen bakım görevlileri ve sorumlu bakım görevlilerini ayarlamak için kullanabilirsiniz. 


## <a name="create-workers"></a>Çalışanlar oluştur

1. **Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Çalışanlar**'ı seçin.
2. Listeye yeni bir çalışan eklemek için **Yeni**'yi seçin.
3. **Çalışan** alanında çalışanı seçin.
4. İş emirlerinde çalışanı planlamak için **Etkin** seçeneğini **Evet** olarak ayarlayın.

    **Genel** hızlı sekmesinde, çalışan için bir kaynak seçilmişse **Kaynak** ve **Açıklama** alanları otomatik olarak doldurulur. **Kaynaklar** sayfasında (**Kuruluş yönetimi** \> **Kaynaklar** \> **Kaynaklar**) çalışanı bir kaynak olarak ayarlayıp bu kaynağa bir takvim tahsis ettiğinizde **Takvim** alanı otomatik olarak doldurulur.

5. **Gruplar** hızlı sekmesinde, **Ekle**'yi ve ardından çalışan için bir bakım görevlisi grubu seçin. Bir çalışan birden fazla grupla ilişkilendirilebilir.
6. Standart kurulumda bir çalışanın bir grupla ilişkisi grubu eklediğiniz tarihte başlar ve hiçbir zaman sona ermez. Bu tarih **Etkinlik tarihi** alanında gösterilir. **Etkinlik tarihi** alanını görmek için **Görünüm** \> **Tümü**'nü seçin. Çalışanın bir grupla ilişkisinin belirli bir dönemle sınırlanması gerekiyorsa bu dönemi tanımlamak için **Etkinlik tarihi** ve **Bitiş tarihi** alanlarını kullanın.
7. **İşlem yapılacak yerleşimler** hızlı sekmesinde **Ekle**'yi ive ardından bakım görevlisi için bir işlem yapılacak yerleşim seçin. Ayrıca çalışan için birincil işlem yapılacak yerleşimi belirtin.

    > [!NOTE]
    > Bir çalışana işlem yapılacak yerleşimler eklediğinizde bu işlem yapılan yerleşimlerle ilgili tüm etkin kıymetler **Etkin kıymetlerim** ve **Etkin işlem yapılacak yerleşimlerim** gibi çeşitli menü öğelerinde görünür. Ayrıca yeni bir kıymet, bakım talebi veya iş emri oluşturduğunuzda gösterilen kıymet aramalarında da görünür.

    **Ayrıntılar** hızlı sekmesindeki alanlar bakım görevlisi gruplarının ve seçili bakım çalışanının ilgili olduğu işlem yapılacak yerleşimlerin sayısını gösterir.

## <a name="create-worker-groups"></a>Çalışan grupları oluştur

1. **Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Bakım görevlisi grupları**'nı seçin.
2. Listeye bir çalışan grubu eklemek için **Yeni**'yi seçin.
3. **Bakım çalışanı grubu** alanına bir grup kimliği girin.
4. **Ad** alanına, bir ad girin.
5. **Çalışanlar** hızlı sekmesinde, **Ekle**'yi ve ardından çalışan grubu için bir bakım görevlisi grubu seçin. **Etkinlik tarihi** ve **Bitiş tarihi** alanları hakkında bilgi için önceki yordamda adım 6'ya bakın.
6. Bir kaynak grubunun seçili bakım görevlisi grubuyla ilgili olması gerekiyorsa **Kaynak gruptan kopyala**'yı seçin. **Grup** alanında takvim ayarlarının kopyalanacağı kaynak grubu seçin. Ardından **Çalışan grubu** alanında kaynak grubunun takvim ayarlarının kopyalanacağı çalışan grubunu seçin. Bu adımı yalnızca iş emri planlaması sırasında bakım görevlilerinin bir kaynakla (iş merkezi) ilgili takvimi kullanmalarını istiyorsanız kullanın.

    **Ayrıntılar** hızlı sekmesindeki alan seçili bakım çalışanı grubunda ayarlanmış bakım görevlilerinin sayısını gösterir.
