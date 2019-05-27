---
title: Proje gerçek değerlerini Finance and Operations'a nakletmek için doğrudan Project Service Automation'dan proje tümleştirme günlüğüne eşitleme
description: Bu konu proje fiili değerlerini, doğrudan Microsoft Dynamics 365 for Project Service Automation üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571112"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Proje gerçek değerlerini Finance and Operations'a nakletmek için doğrudan Project Service Automation'dan proje tümleştirme günlüğüne eşitleme

[!include[banner](../includes/banner.md)]

Bu konu proje fiili değerlerini, doğrudan Microsoft Dynamics 365 for Project Service Automation üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

Şablon, hareketleri Project Service Automation'dan Finance and Operations'taki bir hazırlama tablosuna eşitler. Eşitleme tamamlandıktan sonra verileri hazırlama tablosundan tümleştirme günlüğüne aktarmanız **gerekir**.

> [!NOTE]
> - Proje fiili değerlerin tümleştirmesi Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 veya sonrasında kullanılabilir.
> - Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.
> - Finance and Operations 7.3.0 kullanıyorsanız ve Project Service Automation'dan masraf hareketlerini görüntülüyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.
> - Project Service Automation'da zaman veya gider hareketlerine satış vergisi tutarları giriyorsanız Project Service Automation Güncelleştirme 7'yi yüklemeniz gerekir. Aksi takdirde vergi tahakkukları, ilişkili zaman veya gider gerçek değerlerine bağlanmaz ve Finance and Operations'a eşitlenmez. Daha fazla bilgi için Desteğe başvurun.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a veri akışı

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gerçek değerleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation'dan alınan proje gerçek değerleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, proje gerçek değerlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Gerçek değerler
    - HareketBağlantıları

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Gerçek değerler                    | Proje gerçek değerleri için tümleştirme varlığı                   |
| Hareket Bağlantıları    | Proje hareketi ilişkileri için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation'da yönetilir ve Finance and Operations'ta proje tümleştirme günlüğüne eşitlenir. Muhasebe, varsayılan mali boyutlar ve deftere nakil kurulumu temel alınarak uygulanır.

### <a name="prerequisites"></a>Ön koşullar

Gerçek değerleri eşitleme işlemi yapılmadan önce, Project Service Automation tümleştirme parametrelerini yapılandırmanız, projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri şablonunda aşağıdaki görevleri tamamlamak için Excel için Microsoft Power Query kullanmanız gerekir:

- Project Service Automation'daki hareket türünü Finance and Operations'taki doğru hareket türüne dönüştürmek. Bu dönüştürme işlemi zaten Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanımlıdır.
- Project Service Automation'daki faturalama türünü Finance and Operations'ta doğru faturalama türüne dönüştürmek. Bu dönüştürme işlemi zaten Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanımlıdır. Sonrasında faturalama türü **Project Service Automation tümleştirme parametreleri** sayfasındaki yapılandırmaya göre satır özelliğine eşlenir.
- Bu şablonla eşitlenmesi gereken belirli kaynak kuruluş birimlerine filtre uygulamak.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance and Operations'a eşitlenecekse sözleşme kuruluş birimini Finance and Operations'ta doğru tüzel kişiliğe dönüştürmeniz gerekir. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanıtım verilerine göre bir koşullu sütun tanımlanır. Son eklenen koşullu sütunu doğru tüzel kişiliklerle güncelleştirmeniz gerekir. Aksi takdirde, bir tümleştirme hatası meydana gelebilir veya doğru olmayan gerçek değer hareketleri Finance and Operations'a aktarılabilir.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance and Operations'a eşitlenmeyecekse son eklenen koşullu sütunu şablonunuzdan silmeniz gerekir. Aksi takdirde, bir tümleştirme hatası meydana gelebilir veya doğru olmayan gerçek değer hareketleri Finance and Operations'a aktarılabilir.

#### <a name="contract-organizational-unit"></a>Sözleşme kuruluş birimi
Şablondaki eklenen koşullu sütunu güncelleştirmek için eşlemeyi açmak üzere **Eşle** okuna tıklayın. Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

- Power Query'de varsayılan Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** bölümünden son **Eklenen Koşul**'u seçin. **İşlev** girişinde **USSI** öğesini tümleştirmeyle kullanılacak tüzel kişiliğin adıyla değiştirin. **İşlev** girişine ihtiyaç duyduğunuz kadar ek koşullar ekleyin ve **USMF** öğesindeki **else** koşulunu doğru tüzel kişilikle güncelleştirin.
- Yeni bir şablon oluşturuyorsanız şirketlerarası zaman ve giderleri desteklemek için ilgili sütunu eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütuna **TüzelKişilik** gibi bir ad verin. Sütun için şu koşulu girin: where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \< organizasyon birimi\>, then \<tüzel kişiliği girin\>; else null.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösterilmektedir. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Şablon eşleme](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation'dan tümleştirdikten sonra hazırlama tablosundan içe aktarma

Hazırlama tablosu periyodik işleminden içe aktarma, gerçek değerlerin Project Service Automation'dan Finance and Operations'a eşitlenmesinden sonra çalıştırılmalıdır. Bu işlem, hazırlama tablosundan proje hareketlerini, muhasebenin uygulandığı ve içe aktarılan hareketlerin deftere nakledilebildiği Project Service Automation tümleştirme günlüğüne aktarır. Bu işlemi toplu iş modunda çalıştırmanızı öneririz ve isteğe bağlı olarak yinelenen bir toplu iş halinde çalıştırılacak şekilde ayarlayabilirsiniz.

## <a name="update-actuals-from-finance-and-operations"></a>Finance and Operations'tan alınan gerçek değerleri güncelleştirme

### <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve temel görevler, deftere nakledilen proje hareketleri için fiş numarasını ve satış vergilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri güncelleştirmesi (Fin and Ops'tan PSA'ya)
- **Projedeki görevlerin adı:**

    - Gerçek değerler 
    - Hareket Bağlantıları

### <a name="entity-set"></a>Varlık kümesi

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Proje gerçek değerleri için tümleştirme varlığı                   | Gerçek değerler                    |
| Proje hareketi ilişkileri için tümleştirme varlığı | Hareket Bağlantıları    |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation'da yönetilir ve Finance and Operations'ta proje tümleştirme günlüğüne eşitlenir. Gerçek değerler Finance and Operations'a nakledildikten sonra Project Service Automation'da Finance and Operations'tan alınan fiş numarasıyla güncelleştirilir. Satış vergileri Finance and Operations'a eklendiyse Project Service Automation'da yeni vergi tahakkukları oluşturulur.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri güncelleştirme şablonunda aşağıdaki görevleri tamamlamak için Power Query kullanmanız gerekir:

- Finance and Operations'daki hareket türünü Project Service Automation'daki doğru hareket türüne dönüştürmek. Bu dönüştürme zaten Proje gerçek değerleri güncelleştirme (Fin and Ops'tan PSA'ya) şablonunda tanımlıdır.
- Finance and Operations'taki faturalama türünü Project Service Automation'daki doğru faturalama türüne dönüştürmek. Bu dönüştürme zaten Proje gerçek değerleri güncelleştirme (Fin and Ops'tan PSA'ya) şablonunda tanımlıdır.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Şablon eşleme](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
