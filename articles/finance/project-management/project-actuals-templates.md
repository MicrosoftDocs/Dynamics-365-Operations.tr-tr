---
title: Proje gerçek değerlerini Finance and Operations'a nakletmek için doğrudan Project Service Automation'dan proje tümleştirme günlüğüne eşitleme
description: Bu konuda, proje gerçek değerlerini doğrudan Microsoft Dynamics 365 Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250542"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Proje gerçek değerlerini Finance and Operations'a nakletmek için doğrudan Project Service Automation'dan proje tümleştirme günlüğüne eşitleme

[!include[banner](../includes/banner.md)]

Bu konu proje fiili değerlerini, doğrudan Dynamics 365 Project Service Automation üzerinden Dynamics 365 Finance üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

Şablon, hareketleri Project Service Automation'dan Finance'teki bir hazırlık tablosuna eşitler. Eşitleme tamamlandıktan sonra verileri hazırlama tablosundan tümleştirme günlüğüne aktarmanız **gerekir**.

> [!NOTE]
> - Proje gerçek değerlerinin tümleştirilmesi, sürüm 8.0.1'den itibaren kullanılabilir.
> - Enterprise edition 7.3.0 kullanıyorsanız KB 4132657 ve KB 4132660'yı yükledikten sonra proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.
> - Sürüm 7.3.0'ı kullanıyorsanız ve masraf hareketlerini Project Service Automation'dan çağırıyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.
> - Project Service Automation'da zaman veya gider hareketlerine satış vergisi tutarları giriyorsanız Project Service Automation Güncelleştirme 7'yi yüklemeniz gerekir. Aksi takdirde vergi tahakkukları, ilişkili zaman veya gider gerçek değerlerine bağlanmaz ve Finance'e eşitlenmez. Daha fazla bilgi için Desteğe başvurun.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e veri akışı

Project Service Automation ile Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gerçek değerleri hakkındaki verilerin Project Service Automation'dan Finance'e akışına olanak tanır.

Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation'dan alınan proje gerçek değerleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, Project Service Automation'dan alınan proje gerçek değerlerini Finance ile eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Gerçek değerler
    - HareketBağlantıları

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                   |
|----------------------------|----------------------------------------------------------|
| Gerçek değerler                    | Proje gerçek değerleri için tümleştirme varlığı                   |
| Hareket Bağlantıları    | Proje hareketi ilişkileri için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri, Project Service Automation'da yönetilir ve Finance'te proje tümleştirme günlüğüne eşitlenir. Muhasebe, varsayılan mali boyutlar ve deftere nakil kurulumu temel alınarak uygulanır.

### <a name="prerequisites"></a>Ön koşullar

Gerçek değerleri eşitleme işlemi yapılmadan önce, Project Service Automation tümleştirme parametrelerini yapılandırmanız, projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri şablonunda aşağıdaki görevleri tamamlamak için Excel için Microsoft Power Query kullanmanız gerekir:

- Project Service Automation'daki hareket türünü Finance'teki doğru hareket türüne dönüştürün. Bu dönüştürme işlemi zaten Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanımlıdır.
- Project Service Automation'daki faturalama türünü Finance'te doğru faturalama türüne dönüştürün. Bu dönüştürme işlemi zaten Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanımlıdır. Sonrasında faturalama türü **Project Service Automation tümleştirme parametreleri** sayfasındaki yapılandırmaya göre satır özelliğine eşlenir.
- Bu şablonla eşitlenmesi gereken belirli kaynak kuruluş birimlerine filtre uygulamak.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance'e eşitlenecekse sözleşme kuruluş birimini Finance'te doğru tüzel kişiliğe dönüştürmeniz gerekir. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanıtım verilerine göre bir koşullu sütun tanımlanır. Son eklenen koşullu sütunu doğru tüzel kişiliklerle güncelleştirmeniz gerekir. Aksi takdirde, bir tümleştirme hatası meydana gelebilir veya doğru olmayan gerçek değer hareketleri Finance'e aktarılabilir.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance'e eşitlenmeyecekse son eklenen koşullu sütunu şablonunuzdan silmeniz gerekir. Aksi takdirde, bir tümleştirme hatası meydana gelebilir veya doğru olmayan gerçek değer hareketleri Finance'e aktarılabilir.

#### <a name="contract-organizational-unit"></a>Sözleşme kuruluş birimi
Şablondaki eklenen koşullu sütunu güncelleştirmek için eşlemeyi açmak üzere **Eşle** okuna tıklayın. Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

- Power Query'de varsayılan Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** bölümünden son **Eklenen Koşul**'u seçin. **İşlev** girişinde **USSI** öğesini tümleştirmeyle kullanılacak tüzel kişiliğin adıyla değiştirin. **İşlev** girişine ihtiyaç duyduğunuz kadar ek koşullar ekleyin ve **USMF** öğesindeki **else** koşulunu doğru tüzel kişilikle güncelleştirin.
- Yeni bir şablon oluşturuyorsanız şirketlerarası zaman ve giderleri desteklemek için ilgili sütunu eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütuna **TüzelKişilik** gibi bir ad verin. Sütun için şu koşulu girin: where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \< organizasyon birimi\>, then \<tüzel kişiliği girin\>; else null.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösterilmektedir. Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Şablon eşleme](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation'dan tümleştirdikten sonra hazırlama tablosundan içe aktarma

Hazırlık tablosu periyodik işleminden İçe Aktarma, gerçek değerlerin Project Service Automation'dan Finance'e eşitlenmesinden sonra çalıştırılmalıdır. Bu işlem, hazırlama tablosundan proje hareketlerini, muhasebenin uygulandığı ve içe aktarılan hareketlerin deftere nakledilebildiği Project Service Automation tümleştirme günlüğüne aktarır. Bu işlemi toplu iş modunda çalıştırmanızı öneririz. İsteğe bağlı olarak, yinelenen bir toplu iş halinde çalıştırılacak şekilde ayarlayabilirsiniz.

## <a name="update-actuals-from-finance"></a>Finance'teki gerçek değerleri güncelleştirme

### <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve temel görevler, Finance'ten alınarak deftere nakledilen proje hareketleri için fiş numarasını ve satış vergilerini Project Service Automation ile eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri güncelleştirmesi (Fin and Ops'tan PSA'ya)
- **Projedeki görevlerin adı:**

    - Gerçek değerler 
    - HareketBağlantıları

### <a name="entity-set"></a>Varlık kümesi

| Finans                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Proje gerçek değerleri için tümleştirme varlığı                   | Gerçek değerler                    |
| Proje hareketi ilişkileri için tümleştirme varlığı | Hareket Bağlantıları    |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri, Project Service Automation'da yönetilir ve Finance'te proje tümleştirme günlüğüne eşitlenir. Gerçek değerler, Finance'e nakledildikten sonra Project Service Automation'da Finance'ten alınan fiş numarasıyla güncelleştirilir. Satış vergileri Finance'e eklendiyse Project Service Automation'da yeni vergi tahakkukları oluşturulur.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri güncelleştirme şablonunda aşağıdaki görevleri tamamlamak için Power Query kullanmanız gerekir:

- Finance'teki hareket türünü Project Service Automation'daki doğru hareket türüne dönüştürün. Bu dönüştürme zaten Proje gerçek değerleri güncelleştirme (Fin and Ops'tan PSA'ya) şablonunda tanımlıdır.
- Finance'teki faturalama türünü Project Service Automation'da doğru faturalama türüne dönüştürün. Bu dönüştürme zaten Proje gerçek değerleri güncelleştirme (Fin and Ops'tan PSA'ya) şablonunda tanımlıdır.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşlemede Finance'ten Project Service Automation'a eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Şablon eşleme](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
