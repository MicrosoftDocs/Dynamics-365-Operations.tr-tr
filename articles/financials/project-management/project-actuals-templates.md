---
title: "Proje gerçek değerlerini Finance and Operations'ta deftere nakletmek üzere Project Service Automation'dan proje tümleştirme günlüğüne doğrudan eşitleme"
description: "Bu konu, proje gerçek değerlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Proje gerçek değerlerini Finance and Operations'ta deftere nakletmek üzere Project Service Automation'dan proje tümleştirme günlüğüne doğrudan eşitleme

Bu konu, proje gerçek değerlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır.

Şablon, Project Service Automation'daki hareketleri Finance and Operations'taki bir hazırlama tablosuna eşitler. Eşitleme tamamlandıktan sonra, hazırlama tablosundan tümleştirme günlüğüne aktarma yapmanız gerekir.

> [!NOTE]
> Proje gerçek değerleri tümleştirmesi, Dynamics 365 for Finance and Operations sürüm 8.01'de mevcuttur.

> [!NOTE]
> Project Service Automation'da zaman veya gider hareketlerine satış vergisi tutarları giriyorsanız, Project Service Automation Güncelleştirme 7'yi yüklemeniz gerekir. Bu güncelleştirme yüklenmezse, vergi tahakkukları, ilişkili zaman veya gider gerçek değerlerine bağlanmaz ve Finance and Operations'a eşitlenmez. Daha fazla bilgi için Destek ekibiyle iletişime geçin.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a veri akışı

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gerçek değerleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, proje gerçek değerlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

-  **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri (PSA'dan Fin and Ops'a)

-  **Projedeki görevlerin adı:** 
    - Gerçek değerler 
    - HareketBağlantıları

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Gerçek değerler                         | Proje gerçek değerleri için tümleştirme varlığı                      |
| Hareket Bağlantıları         | Proje hareketi ilişkileri için tümleştirme varlığı    |

## <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation'da yönetilir ve Finance and Operations'tan proje tümleştirme günlüğüne eşitlenir. Muhasebe, varsayılan mali boyutlar ve deftere nakil kurulumu temel alınarak uygulanır.

## <a name="preconditions"></a>Ön koşullar

Gerçek değerleri eşitleme işlemi yapılmadan önce, Project Service Automation tümleştirme parametrelerini yapılandırmanız, projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Proje gerçek değerleri şablonunda şu işlemler için Microsoft Power Query kullanmanız gerekir:
- Project Service Automation **hareket türünü** Finance and Operations'taki uygun **hareket türüne** dönüştürmek. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda zaten bu dönüştürme tanımlı.
- Project Service Automation **faturalama türünü** Finance and Operations'taki uygun **faturalama türüne** dönüştürmek. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda zaten bu dönüştürme tanımlı. Bunun ardından, faturalama türü, Dynamics 365 for Project Service Automation tümleştirme parametreleri formundaki yapılandırmaya göre **satır özelliğine** eşlenir.
- Bu şablonla eşitlenecek belirli **Kaynak kuruluş birimlerine** filtre uygulamak.
- **Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri** Finance and Operations'a eşitlenecekse, **sözleşme kuruluş birimini** Finance and Operations'ta uygun **tüzel kişiliğe** dönüştürmeniz gerekir. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda tanıtım verilerine göre tanımlanmış bir koşullu sütun vardır. Son eklenen koşul sütununu uygun tüzel kişiliklere güncelleştirmeniz gerekir. Bu yapılmadığı takdirde bir tümleştirme hatası olabilir veya gerçek değer hareketleri Finance and Operations'a yanlış aktarılabilir.
- **Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri** Finance and Operations'a eşitlenmeyecekse, son eklenen koşul sütununu şablonunuzdan silmeniz gerekir. Bu yapılmadığı takdirde bir tümleştirme hatası olabilir veya gerçek değer hareketleri Finance and Operations'a yanlış aktarılabilir.

### <a name="contract-organizational-unit"></a>Sözleşme Kuruluş Birimi
Şablondaki eklenen koşul sütununu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın. Gelişmiş Sorgu ve Filtreleme'yi açmak için seçin.
- Varsayılan Microsoft Project gerçek değerleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, **Uygulanan Adımlar** bölümündeki son **Eklenen Koşul**'u seçin. **İşlev** girişinde **USSI**'yı, tümleştirmeyle kullanılacak **Tüzel kişiliğin** adıyla değiştirin. Gerektiğinde **İşlev** girişine daha fazla koşul ekleyin ve **USMF**'den **else** koşulunu uygun **Tüzel kişiliğe** güncelleştirin.
- Yeni bir şablon oluşturuyorsanız, şirketlerarası zaman ve giderleri desteklemek için bu sütunu eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin (örneğin TüzelKişilik). Sütun için şu koşulu girin: where if msdyn_contractorganizationalunitid.msdyn_name is <organizational unit>, then <enter the Legal entity>; else null.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Şablon eşleme](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Hazırlama tablosundan içe aktar

Hazırlama tablosu periyodik işleminden içe aktarma, gerçek değerlerin Project Service Automation'dan Finance and Operations'a eşitlenmesinden sonra çalıştırılmalıdır. Bu işlem, hazırlama tablosundan proje hareketlerini, muhasebenin uygulandığı ve içe aktarılan hareketlerin deftere nakledilebildiği Project Service Automation tümleştirme günlüğüne aktarır. Bu işlemi toplu iş modunda çalıştırmanız önerilir ve isteğe bağlı olarak yinelenen bir toplu iş halinde çalıştırılacak şekilde ayarlanabilir.

## <a name="update-actuals"></a>Gerçek Değerleri Güncelleştirme

Aşağıdaki şablon ve temel görevler, deftere nakledilen proje hareketleri için fiş numarasını ve satış vergilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:

-  **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri güncelleştirmesi (Fin and Ops'tan PSA'ya)
-  **Projedeki görevlerin adı:** 
     - Gerçek değerler 
     - Hareket Bağlantıları

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Proje gerçek değerleri için tümleştirme varlığı                         | Gerçek değerler                           |
| Proje hareketi ilişkileri için tümleştirme varlığı       | Hareket Bağlantıları           |

## <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation'da yönetilir ve Finance and Operations'tan proje tümleştirme günlüğüne eşitlenir. Finance and Operations'ta deftere nakledildikten sonra gerçek değerler Project Service Automation'da Finance and Operations'tan alınan fiş numarasıyla güncellenir. Finance and Operations'a satış vergileri eklendiyse, Project Service Automation'da yeni vergi gerçek değerleri oluşturulur.

## <a name="power-query"></a>Power Query

Proje gerçek değerleri güncelleştirme şablonunda şu işlemler için Microsoft Power Query kullanmanız gerekir:
- Finance and Operations **hareket türünü** Project Service Automation'daki uygun **hareket türüne** dönüştürmek. Proje gerçek değerleri güncelleştirmesi (Fin and Ops'tan PSA'ya) şablonunda zaten bu dönüştürme tanımlı.
- Finance and Operations **faturalama türünü** Project Service Automation'daki uygun **faturalama türüne** dönüştürmek. Proje gerçek değerleri güncelleştirmesi (Fin and Ops'tan PSA'ya) şablonunda zaten bu dönüştürme tanımlı.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Şablon eşleme](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




