---
title: İş emri havuzları
description: Bu makalede Varlık Yönetimi'nde iş emri havuzlarıyla çalışma açıklanmaktadır.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc9eaf82c2f3336f8c3400fcd3f1165ed4fa56d8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014983"
---
# <a name="work-order-pools"></a>İş emri havuzları

[!include [banner](../../includes/banner.md)]


Ortak bir şeyler içeren iş emirlerini gruplamak için iş emri havuzlarını kullanabilirsiniz. Aşağıda, iş emri havuzları oluşturabileceğiniz şeylerle ilgili bazı örnekler yer almaktadır:

- İş ekipleri, örneğin Bakım Ekibi, A veya Bakım Ekibi B  

- Profesyonel yetenekler, örneğin elektrikçi veya tesisatçı  

- Fiziksel yerleşimler  

- Zaman planlamaları, örneğin hafta veya diğer dönemler  

Gerektiğinde, bir iş emrini birden fazla iş emri havuzuna koyabilirsiniz.


## <a name="create-a-work-order-pool"></a>İş emri havuzu oluşturma

**Tüm iş emri havuzları** veya **Etkin iş emri havuzları** liste sayfasında, iş emri havuzlarınızın genel görünümünü alabilir ve yeni havuzlar oluşturabilirsiniz.

1. **Varlık yönetimi** > **İş emri havuzları** > **Tüm iş emri havuzları** veya **Etkin iş emri havuzları**'nı seçin.

2. **Yeni**'yi seçin.

3. **Havuz** alanına iş emri havuzu için bir kimlik girin.

4. **Ad** alanına, bir ad girin.

5. İş emri havuzunun etkin olduğunu belirtmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.

6. İş emirlerinin otomatik olarak iş emri havuzundan kaldırılması için **İş emri ilişkilerini sil** seçeneğini **Evet** olarak ayarlayın.

7. **Yaşam döngüsü durumunu sil** alanında, iş emri yaşam döngüsü durumunu seçin. Örneğin, bir iş emrini tamamlamaya yönelik iş emri yaşam döngüsü durumu, iş emri havuzlarının ilişkilerini otomatik olarak silecek şekilde ayarlanabilir.

    İş siparişi havuzunuza iş emirlerini hemen eklemeye başlayabilirsiniz.

8. **İş emirleri** hızlı sekmesinde **Satır ekle**'yi seçin.

9. **İş emri** alanında bir iş emri seçin. İlgili alanlar otomatik olarak güncelleştirilir.

10. Daha fazla iş emri eklemek için 8 ile 9. adımlar arasındaki işlemleri tekrarlayın.

11. Eklediğiniz iş emirlerinin belirli bir sırada gerçekleştirilmesi gerekiyorsa, sıralamayı belirtmek için **Sıralama düzeni** alanına **1**, **2**, **3**, vb. sayılarını girebilirsiniz.

12. İş emri havuzuna dahil edilen tüm iş emirlerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **İlgili iş emri havuzunu görüntüle** grubunda **İş emirleri**'ni seçerek **Tüm iş emirleri** liste sayfasını açın.

13. Bakım zamanlaması, zamanlanmamış iş emirleri ve zamanlanmış iş emirleri için kapasite yükünü hesaplamak ve görüntülemek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde, **İlgili iş emri havuzunu görüntüle** grubunda **Kapasite yükünü** seçerek **Kapasite yükünü hesapla** iletişim kutusunu açın.

14. Bakım zamanlaması, zamanlanmamış iş emirleri ve zamanlanmış iş emirleriyle ilgili maddeler için (yedek parçalar ve diğer gerekli maddeler) tahminleri hesaplamak ve görüntülemek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde, **İlgili iş emri havuzunu görüntüle** grubunda **Madde tahminini** seçerek **Madde tahminini hesapla** iletişim kutusunu açın.

15. İş emri havuzundaki iş emirleriyle ilgili satınalma taleplerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **Tedarik** grubunda **İş emri satınalma talebi**'ni seçerek **İş emri satınalma talebi** liste sayfasını açın.

16. İş emri havuzundaki iş emirleriyle ilgili satınalma siparişlerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **Tedarik** grubunda **İş emri satınalma işlemi**'ni seçerek **İş emri satınalma işlemi** liste sayfasını açın.

>[!NOTE]
>Bir iş emri havuzu artık iş planınızla ilgili değilse, **İş emri havuzu** sayfasındaki liste görünümünde havuz için **Etkin** seçeneğini **Hayır** olarak ayarlayın.

Tüm iş emri satırlarını silmek için, **İş emri ilişkilerini sil** seçeneğini **Evet** olarak ayarlayın. Bu seçenek, örneğin, daha sonra diğer iş emirleri için kullanabileceğiniz boş bir havuz oluşturmak istediğinizde yararlıdır. Daha sonra yeni iş emri ilişkileri oluşturmak için iş emri havuzunu kullanmaya hazır olduğunuzda **İş emri ilişkilerini sil** seçeneğini **Hayır** olarak ayarlamayı unutmayın.

Aşağıdaki şekilde **İş emri havuzu** liste sayfası örneği gösterilmektedir.

![Şekil 1.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>İş emri havuzuna iş emri ekleme

Önceki bölümde açıklandığı gibi, havuzu oluştururken iş emri havuzuna iş emirleri ekleyebilirsiniz. Ayrıca, **Tüm iş emirleri** veya **Etkin iş emirleri** listesi sayfasındaki iş emri havuzuna da iş emirleri ekleyebilirsiniz.

1. İş emrini seçin ve sonra Eylem bölmesinde **İş emri** sekmesinde, **Koru** grubunda **İş emri havuzu** öğesini seçin.

2. Listeden iş emrini seçin ve **İş emri havuzu**'na tıklayın.

3. **İş emri havuzunu koru** iletişim kutusunda, **Ekle/Kaldır** alanında, **Ekle**'yi seçin.

4. **Havuz** alanında iş emri havuzunu seçin.

5. **Tamam**'ı seçin.

6. Belirli bir sırada eklediğiniz iş emrini iş emri havuzuna koymak için **Tüm işemri havuzları** veya **Etkin iş emri havuzları** liste sayfasında havuzu ve ardından **Düzenle**'yi seçin. Ardından **İş emri havuzu** sayfasında **İş emirleri** hızlı sekmesinde, havuza dahil edilen iş emirlerinin sıralama düzenini ayarlamak için **Sıralama düzeni** alanını kullanın.

Bir iş emrini iş emri havuzundan kaldırmak için bu adımları tekrarlayın ancak adım 3'te **Kaldır**'ı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]