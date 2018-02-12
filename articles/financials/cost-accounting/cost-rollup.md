---
title: "Maliyet yuvarlama ilkesi ve genel gider hesaplaması"
description: "Bu konu, ikincil maliyet öğelerinin doğru düzeyini belirlemek ve kuruluşun raporlamasına ve maliyet izlemesine uygun maliyet öğeleri ve maliyet yuvarlama kuralları oluşturmak hakkında bilgi sağlar."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 044a943eeba91f5dbebd4dcd70bc8152c4109037
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="cost-rollup-policy-and-overhead-calculation"></a>Maliyet yuvarlama ilkesi ve genel gider hesaplaması 

[!include[banner](../includes/banner.md)]

Maliyet muhasebesi, maliyet akışının bir kuruluş içerisinde teslim edilen ürünler ve hizmetlerle nasıl ilişkili olduğu hakkında bilgiler sağlar. Maliyet saydamlığını görmek için, uygun tahsisat tabanına dayalı maliyet nesneleri arasında maliyet tahsisatı elde etmek önemlidir. Varsayılan olarak, maliyet tahsisatı, bazı durumlarda istenilen ancak dikkate alınması gereken birkaç olası etkiye sahip birincil maliyet öğesi için elde edilir.

-   Ek maliyet nesneleri, genel gider hesaplamasından sonra birincil maliyet öğesi için sıfır bakiye ile kapanır.

-   Genel gider hesaplaması tarafından oluşturulan maliyet girdilerinin hacmi çok yüksek olabilir.

-   Maliyet nesneleri arasında maliyet akışını izlemek mümkün değildir.

Maliyet muhasebesi, bu ektilerin önüne geçmek için maliyet tahsisatının kuruluşunuzun yönetimsel raporlama gereksinimlerine uyacak şekilde yapılandırılmasını sağlar. Bu konu, ikincil maliyet öğelerinin doğru düzeyini belirlemek ve kuruluşun raporlamasına ve maliyet izlemesine uygun maliyet öğeleri ve maliyet yuvarlama kuralları oluşturmayı ele alır.

> [!NOTE]
> Raporlama gereksinimleri değişirse yapılandırmaları değiştirebilirsiniz.

## <a name="example-of-cost-rollup-policy-setup"></a>Maliyet yuvarlama ilke kurulumu örneği

Bir kurulun, aşağıdaki 4 maliyet merkezli yapıya sahip olduğunu düşünün.

![Bir kuruluş yapısı örneği](./media/dimension-hierarchy-org.png)

**Maliyet nesnesi boyutu**

| Maliyet merkezleri | Açıklama          |
|--------------|-----------|
| CC001        | İK        |
| CC002        | Finans   |
| CC003        | Montaj  |
| CC004        | Paketleme |

**Maliyet öğesi boyutu**

| Maliyet öğeleri | Açıklama | Türü    |
|---------------|-------------|---------|
| 1001          | Elektrik | Birincil |
| 1002          | Maaşlar    | Birincil |
| 1003          | Reklam | Birincil |

Kuruluşun raporlama gereksinimlerini karşılayan bir boyut hiyerarşisi aşağıdaki gibi ayarlanabilir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut    | Boyut hiyerarşisi türü adı      | Erişim listesi hiyerarşisi |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizasyon             | Maliyet merkezleri | Boyut sınıflandırması hiyerarşisi | Hayır                    |

**Boyut hiyerarşisi**

|              | Boyut üyesi aralıkları |                     |
|--------------|-------------------------|---------------------|
| **Düğümler**        | **Kaynak boyut üyesi**   | **Hedef boyut üyesi** |
| Organizasyon |                         |                     |
| &nbsp;&nbsp;Yönetici             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;İK               | CC002                   | CC002               |
| &nbsp;&nbsp;Üretim               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Paketleme              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Montaj             | CC004                   | CC004               |

İlke gereksinimlerini karşılayan bir boyut hiyerarşisi aşağıdaki gibi ayarlanabilir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut     | Boyut hiyerarşisi türü adı      |
|--------------------------|---------------|------------------------------------|
| Kar ve zarar raporu  | Maliyet öğeleri | Boyut sınıflandırması hiyerarşisi |

**Boyut hiyerarşisi**

|                         | Boyut üyesi aralıkları |                     |
|-------------------------|-------------------------|---------------------|
| Düğümler                   | Kaynak boyut üyesi   | Hedef boyut üyesi |
| Kar ve zarar raporu |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Birincil maliyet                    | 10001                   | 10003               |

Genel muhasebe girişleri işlendikten sonra, maliyet nesnesine dayalı maliyet girdi dengesi aşağıdaki gibi görünür.

|                      | **Maliyet nesnesi** |           |           |           | **Toplam**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Maliyet öğesi**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektrik** | 100,00          | 200.000    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Maaşlar**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Reklam** | 0.00            | 4.000,00  | 0.00      | 0.00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**İstatistiksel boyut**

| İstatistiksel öğeler |    Açıklama   |
|----------------------|------------------|
| SE-1                 | HR hizmetleri      |
| SE-2                 | Finans hizmetleri |

Maliyet nesnesi CC001 İK, birden fazla maliyet nesnesine İK hizmeti katkısında bulunur.

İK hizmetleri aşağıdaki büyük dağılımı tarafından tüketilir.

| Maliyet nesnesi | Açıklama |   HR hizmetleri |
|-------------|-------------|----|
| CC002       | Finans     | 35 |
| CC003       | Montaj    | 55 |
| CC004       | Paketleme   | 10 |

Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunuyor.

Finans hizmetleri aşağıdaki büyük dağılımı tarafından tüketilir.

| Maliyet nesnesi |   Açıklama    |  Finans hizmetleri   |
|-------------|------------------|----|
| CC003       | Montaj         | 65 |
| CC004       | Paketleme        | 35 |

Maliyet tahsisat ilkeleri aşağıdaki gibi ayarlanabilir.

| İlke adı | Açıklama     | Maliyet nesnesi boyut hiyerarşisi | İstatistiksel boyut | Maliyet öğesi boyutu |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Maliyet tahsisatı | Organizasyon                    | İstatistiksel öğeler  | Maliyet öğeleri          |

Maliyet tahsisat kuralları aşağıdaki gibi ayarlanabilir.

| Maliyet nesnesi boyut hiyerarşisi düğümü | Maliyet davranışı | Tahsisat temeli        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Toplam         | **HR hizmetleri**        |
| CC002                                | Toplam         | **Finansal hizmetler** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Maliyetin maliyet merkezleri arasında akışı 
---------------------------------------------------

Maliyetin, kuruluş içerisindeki maliyet merkezlerinde nasıl aktığını öğrenmek istiyorsanız, her bir maliyet merkezi için **İkincil** türde bir maliyet öğesi oluşturabilirsiniz. Bu maliyet öğeleri daha sonra genel gider hesaplaması sırasında maliyet merkezleri arasında bakiyeleri nakletmekte kullanılır.

Maliyet öğesi boyut üyeleri aşağıdaki gibi ayarlanabilir.

| Maliyet öğeleri | Türü          |               |
|---------------|---------------|---------------|
| 1001          | Elektrik   | Birincil       |
| 1002          | Maaşlar      | Birincil       |
| 1003          | Reklam   | Birincil       |
| **SC-CC001**  | **İK**        | **İkincil** |
| **SC-CC002**  | **Finans**   | **İkincil** |
| **SC-CC003**  | **Montaj**  | **İkincil** |
| **SC-CC004**  | **Paketleme** | **İkincil** |

Boyut hiyerarşisi **Kar ve Zarar raporu**'nun, boyut hiyerarşisinin raporlamaları ve ilkeleri tanımlamakta kullanılacak doğru verileri içermesi için yeni boyut üyeleri ile güncelleştirilmesi gerekiyor.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut     | Boyut hiyerarşisi türü adı      |
|--------------------------|---------------|------------------------------------|
| Kar ve zarar raporu  | Maliyet öğeleri | Boyut sınıflandırması hiyerarşisi |

**Boyut hiyerarşisi**

|                         | Boyut üyesi aralıkları |                     |
|-------------------------|-------------------------|---------------------|
| Düğümler                   | Kaynak boyut üyesi   | Hedef boyut üyesi |
| Kar ve zarar raporu |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Birincil maliyet                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;İkincil maliyet                         | **SC-CC001**            | **SC-CC004**        |

Her maliyet merkezinin, karşılık gelen bir **İkincil** maliyet öğesine eşleştiği bir **Maliyet yuvarlama ilkesi** oluşturun.

**Maliyet yuvarlaması ilkeleri**

| İlke adı | Açıklama | Maliyet nesnesi boyut hiyerarşisi | Maliyet öğesi boyut hiyerarşisi |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Maliyet akışı   | Organizasyon                    | Kar ve zarar raporu          |

**Maliyet yuvarlaması kuralları**

| Maliyet nesnesi boyut hiyerarşisi düğümü | Maliyet öğesi boyut hiyerarşisi düğümü | İkincil maliyet öğesi |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Kar ve zarar raporu               | **SC-CC001**           |
| CC002                                | Kar ve zarar raporu               | **SC-CC002**           |
| CC003                                | Kar ve zarar raporu               | **SC-CC003**           |
| CC004                                | Kar ve zarar raporu               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Genel gider hesaplaması gerçekleştir

**Günlük**

| Günlük | Günlük türü:            | Mali takvim dönemi | Yıl | Dönem | Sürüm       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Maliyet tahsisatı günlüğü | Mali                 | 2017    | Dönem 1 | Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1 |

Sistem şimdi **Maliyet yuvarlama ilkesi**'ni, **Maliyet nesnesi bakiye günlüğü girdileri**'ni oluşturduğunda uygulayacaktır.

**Maliyet nesnesi bakiyesi günlük girişleri**

| Muhasebeleşme tarihi | Maliyet nesnesi | Açıklama  | Maliyet öğesi | Açıklama |  Tutar |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31-01-2017      | CC001       | İK           | SC-CC001 | İK        | 10.100,00 |
| 31-01-2017      | CC002       | Finans      | SC-CC002 | Finans   | 17.735,00 |
| 31-01-2017      | CC003       | Montaj     | SC-CC003 | Montaj  | 31.082,75 |
| 31-01-2017      | CC004       | Paketleme    | SC-CC004 | Paketleme | 15.717,25 |

> [!NOTE]
> Günlük girişleri, **Maliyet yuvarlama ilkesi** mevcutsa, bunun üzerindeki kurallara dayanarak oluşturulacaktır. Görüntülenen bakiye, genel gider hesaplamasının bakiyesidir.

Günlük girdilerinden erişilen **Maliyet nenesi maliyeti bakiye günlüğü girdi ayrıntıları** sayfası, bakiyenin nasıl elde edildiğini gösterir.

**Örnek: Maliyet nesnesi CC002 Finans için günlük girişi**

**Maliyet nesnesi maliyet bakiyesi günlük girişi ayrıntıları**

| Maliyet öğesi boyut üyesi | Açıklama |  Tutar   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektrik | 200.000    |
| 1002                          | Maaşlar    | 10.000,00 |
| 1003                          | Reklam | 4.000,00  |
| SC-CC001                      | İK          | 3.535,00  |

**Genel gider hesaplaması tarafından oluşturulan maliyet girişleri**

| Maliyet nesnesi | Açıklama  | Maliyet öğesi   | Açıklama  |        Tutar     |       Muhasebeleşme tarihi     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | İK           | SC-CC001 | İK              | \-10.100,00 | 31-01-2017 |
| CC002       | Finans      | SC-CC001 | İK              | 3.535,00    | 31-01-2017 |
| CC003       | Montaj     | SC-CC001 | İK              | 5.555,00    | 31-01-2017 |
| CC004       | Paketleme    | SC-CC001 | İK              | 1.010,00    | 31-01-2017 |
| CC002       | Finans      | SC-CC002 | Finans         | \-17.735,00 | 31-01-2017 |
| CC003       | Montaj     | SC-CC002 | Finans         | 11.527,75   | 31-01-2017 |
| CC004       | Paketleme    | SC-CC002 | Finans         | 6.207,25    | 31-01-2017 |

**Genel gider hesaplama** tamamlandıktan sonra, sonuçları Microsoft SharePoint Workspace, Excel veya Power BI gibi araçlar kullanarak rapor edebilirsiniz.

## <a name="view-reporting-in-excel"></a>Raporlamayı Excel'de görüntüle 

Boyut hiyerarşileri, veriyi farklı toplama düzeylerinde görmenize olanak sağlar.

Excel içerisinde Power Pivot raporlama örneği.

| **Kar ve zarar raporu** | **Maliyet nesnesi** |                |               |               |  **Toplam**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Birincil maliyet**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;1001                            | 100,00          | 200.000         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                             | 0.00            | 4.000,00       | 0.00          | 0.00          | **4.000,00**  |
|**İkincil maliyet**                            | **-10.100,00**  | **-14.200,00** | **17.082.75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0.00            | \-17.735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
| **Toplam**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

**Maliyet yuvarlama ilkesi** ve **İkincil türdeki maliyet öğeleri**, dahili raporlama için maliyet nesnesi başına birincil maliyeti, **Genel gider hesaplaması**'ndan sonra kalan birincil maliyet olarak bırakmanıza olanak sağlar.

Aynı örnek **Maliyet yuvalarma ilkesi** oluşturmadan gerçekleştirilirse, raporlama sonucu aşağıda gösterilen gibi olur. Maliyet doğru şekilde akar ancak maliyetin maliyet merkezleri arasında nasıl aktığının izlenebilirliği ve bilgileri kaybolur.

| **Kar ve zarar raporu** | **Maliyet nesnesi** |           |               |               |          **Toplam**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Birincil maliyet**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1001                              | 0.00            | 0.00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                             | 0.00            | 0.00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                              | 0.00            | 0.00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**İkincil maliyet**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
| **Toplam**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Kuruluşunuzdaki raporlama ve izlenebilirlik gereksinimlerine bağlı olarak, ikincil maliyet öğelerinin doğru seviyesini belirleyebilir ve ihtiyaçlarınızı karşılayan maliyet yuvarlama kuralları oluşturabilirsiniz.

**Maliyet tahsisatı** ve **Maliyet yuvarlama ilkeleri** arasındaki net ayrım, birbirlerini etkilemeyen sürekli güncelleştirme yapma esnekliği sağlar.



## <a name="see-also"></a>Ayrıca bkz.
-  [Maliyet nesnesi boyutları](cost-objects.md)
-  [Maliyet öğesi boyutları](cost-elements.md)
-  [Boyut hiyerarşileri](dimension-hierarchy.md)
-  [Genel gider hesaplaması](overhead-calculation.md)

