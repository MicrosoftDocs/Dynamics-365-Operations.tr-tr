---
title: CFO çalışma alanına mali boyutlar ekleme
description: Bu konu, genel muhasebe ve bütçe raporları için kullanılabilmeleri amacıyla CFO çalışma alanına mali boyutların nasıl ekleneceğini açıklar.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b42fc4f0e299dc785ef465efc54286effccfb92b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823848"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>CFO çalışma alanına mali boyutlar ekleme

[!include [banner](../includes/banner.md)]

Bu konu, genel muhasebe ve bütçe raporları için kullanılabilmeleri amacıyla Mali İşler Müdürü (CFO) çalışma alanına mali boyutların nasıl ekleneceğini açıklar. CFO çalışma alanı bir **Genel bakış** sekmesine ve bir **Mali** sekmesine sahiptir. Bu iki sekmedeki raporlar iki ölçüt tarafından desteklenir: LedgerActivityMeasure ve BudgetActivityMeasure. Bu iki ölçü ve DimensionCombinationEntity varlığı arasında ilişki vardır. Bu nedenle, boyutları seçebilirsiniz.

1. Finance'da **Varlık Deposu** sayfasında, **LedgerActivityMeasure** ve **BudgetActivityMeasure** ölçülerini güncelleştirin.
2. Microsoft Visual Studio'da, Uygulama Gezgini'ni açın ve **LedgerCFO** aratın.
3. **Kaynaklar** altında, **LedgerCFOWorkspacePBIX** açın.
4. Kaynak Microsoft Power BI masaüstünde açıldığında **Veri Al**'ı seçin, **SQL Server veritabanı**'nı seçin ve daha sonra **Bağlan**'ı seçin.
5. Sunucu adını girin ve veritabanı olarak **AxDW** girin. **DirectQuery** seçin ve daha sonra **Tamam**'ı seçin.
6. **LedgerActivityMeasure\_DimensionCombination** arayın ve seçin, daha sonra **Yükle**'yi seçin.

    > [!TIP]
    > **Alanlar** listesinde kolayca ayırt edebilmek için **Mali boyutlar** tablosunun adını değiştirin.

7. **İlişkileri Yönet**'i seçin ve daha sonra **Yeni**'yi seçin.
8. İlk alanda **Genel Muhasebe Faaliyetleri**'ni seçin ve **LedgerDimension**'u seçin.
9. İkinci alanda **LedgerActivityMeasure\_DimensionCombination** (veya tablonu adını değiştirdiyseniz **Mali boyutlar**) seçin. **DimensionCombinationRECID** başlığını seçin.
10. **Asallık** alanında **Birçoktan Bire**'yi seçin.
11. **Çapraz filtre yönü** değerini **Tek** olarak değiştirin.
12. **Bu ilişkiyi etkin yap** ve **Referans tutarlığını kabul et**'i seçin, **Tamam**'ı seçin ve daha sonra **Kapat**'ı seçin.

    [![Bir ilişki oluştur](./media/Create-relationship.png)](./media/Create-relationship.png)

13. **Alanlar** listesinde, tabloyu veya kullanılabilir mali boyutları görebilmeniz gerekir. İstediğiniz mali boyutları raporlama düzeyi filtrelerine sürükleyin.
14. Değişikliklerinizi kaydedin.
15. Uygulama Nesne Ağacı (AOT) içerisinde projeni sağ tıklayın ve sonra **Eşitle**'yi seçin.
16. Projenizi oluşturun ve sonra sonuçları görmek için uygulamayı açın.

    [![Tamamlanan çalışma alanı](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]