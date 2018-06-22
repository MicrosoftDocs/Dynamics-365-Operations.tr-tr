---
title: "Project Service Automation tümleştirme parametreleri"
description: "Project Service Automation'ı Dynamics 365 for Finance and Operations'la tümleştirirken verilerin nasıl varsayılan kılınacağını yapılandırabilirsiniz."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation tümleştirme parametreleri

**Project Service Automation tümleştirme parametreleri** sayfasında, Project Service Automation'ı Finance and Operations'la tümleştirirken verilerin nasıl varsayılan kılınacağını yapılandırabilirsiniz. Project Service Automation'daki projelerin Finance and Operations'ta başarıyla eşitlenebilmesi için aşağıdakilerin ayarlanması gerekir.

> [!NOTE]
> Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.




| **Sekme**                      | **Alan**                          | **Açıklama**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Genel**                  | **Varsayılan proje türü**               | Tümleştirme şablonunda bir varsayılan değer belirtmediyseniz, projeler Project Service Automation'dan eşitlenirken **Proje türü** için varsayılan değeri seçin. Eşitleme sırasında yeni projelerin **Proje türü** bu değere ayarlı olacaktır ve bu değer, proje sözleşme satırları Project Service Automation'dan eşitlenirken güncellenebilir.               |
| **Genel**                  | **Süre kategorisi**                      | Project Service Automation'dan saat tahminleri eşitlenirken **Zaman kategorisi** için varsayılan değeri seçin. Eşitleme sırasında, saat tahminleri ve saat gerçek değerleri Project Service Automation'dan eşitlenirken Finance and Operations'taki yeni proje saat tahminlerinin **Kategori** ayarı bu değeri alacaktır.   |
| **Genel**                  | **Ücret kategorisi**                       | Project Service Automation'dan ücret gerçek değerleri eşitlenirken **Ücret kategorisi** için varsayılan değeri seçin. Eşitleme sırasında, ücret gerçek değerleri Project Service Automation'dan eşitlenirken Finance and Operations'taki yeni ücret hareketlerinin **Kategori** ayarı bu değeri alacaktır.          |
| **Proje grubu varsayılanları**   | **Proje türü** | Varsayılan proje grubu ayarlanacak proje türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın. Yapılandırmada belirli bir proje türü yalnızca bir kez seçilebilir.              
|                              | **Proje Grubu**          | Belirtilen proje türü için varsayılan proje grubunu seçin. Tümleştirme şablonunda bir varsayılan değer belirtmediyseniz, Project Service Automation'dan yeni projeler eşitlenirken, **Proje grubu**, proje türüne göre varsayılan olacaktır.  |
| **Faturalama türü varsayılanları**    | **Faturalama türü** | Varsayılan satır özelliği ayarlanacak faturalama türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın. Yapılandırmada belirli bir faturalama türü yalnızca bir kez seçilebilir.          |
|                              | **Satır özelliği**| Belirtilen faturalama türü için varsayılan satır özelliğini seçin. Project Service Automation'dan yeni saat tahminleri, yeni gider tahminleri veya yeni gerçek değerler eşitlenirken, **Satır özelliği**, faturalama türüne göre varsayılan olacaktır.          |
| **İşlev kilitleme**    |                   | Project Service Automation kaynaklı projeler ve sözleşmeler için Finance and Operations'ta devre dışı bırakılacak işlevselliği seçin. Örneğin Finance and Operations'ta sözleşme ve proje düzenleme, iş kırılım yapıları oluşturma ve zaman çizelgeleri girme yeteneklerini devre dışı bırakmayı seçebilirsiniz. Muhasebeyle ilgili alanlar parametre ayarıyla kullanılamaz yapılsa bile, etkin olmaya devam eder. Varsayılan olarak, tüm işlevsellik etkinleştirilir.           |

