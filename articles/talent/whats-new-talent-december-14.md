---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (14 Aralık 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306506"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (14 Aralık 2018)

[!include [banner](includes/banner.md)]

**Derleme 8.1.2085**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes"></a>Değişiklikler

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>US - ACA (uygun eylemi yasası) vergi yılı 2018 1095-B ve C-1095 formlar için desteği

Her yıl, Applicable Large Employers (ALE'ler), her bir tam zamanlı çalışanlarına bir 1095-C sağlamalıdır. Ayrıca, İşveren kendini Sigortalı tedarik sağlıyorsa, (bir ALE farklıysa) 1095 C belirtmeniz gerekir ve bir 1095-(küçük bir İşveren farklıysa) B çalışanlara, tam zamanlı veya yarı zamanlı, sunulan durumu planları birinde. Bu özellik hem 1095-C ve b-1095 için yazdırılabilir formlar sağlar.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>İçe aktarma sırasında HcmPerfJournalEntity üzerinde SubmittedByPersonId alanı yoksayılır

Performans günlük girişlerinde, alma/verme sırasında **Tarafından gönderilen** alanı dikkate alınmaz. Bu değişiklik ile, değer **İçe/dışa aktarılan** alma sistemi içe aktarma dosyasında sağlanan değer güncelleştirilir, dışa aktarma sırasında tablo değeri gösterir.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>'İzin ve devamsızlık' çalışma alanı üzerindeki analiz sekmesi "OpenConnectionError" hatasını sistem Yöneticisi olmayan roller için gösterir.

Bu güncelleştirme ile **Analitik** sekmesini **İzin ve Devamsızlık** çalışma alanında açarken hata verilmez.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Çalışan Self-Servis, Konum hiyerarşisini açılan kutusundan ana düğüm alamıyor

"Alma üst düğüm hatası"nı düzeltmek için ne zaman varolan bir çalışma alanında görüntülenecek konumu hiyerarşi kişiselleştirilmiş ve hiyerarşide bir konumda değişiklik yapıldı.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Konum sayfasında Bordro sekmesini görmek için Sistem Yöneticisi olmak gerekir

Mevcut ayrıcalıkta doğru güvenlik öğelerini dahil etmek için bir değişiklik yapıldı: "Bordro çalışanı ve konum ayrıntısını koru". Bu değişikliğe göre varsayılan olarak, Bordro Yöneticisi, Bordro konumu sayfa alanlarına erişebilir.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Performans gözden geçirmesini yöneticiye gönderirken hata ve %Reviews.PerfPeriod% yer tutucusu, Gönderme talimatlarında kullanılır

%Reviews.PerfPeriod% yer tutucusunu Gönderme talimatlarında kullanırken oluşan "Null Reference" hatasını düzeltmek için bir değişiklik yapıldı.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Workforce Power BI raporu, çalışan kıdem tarihi bir artık gün olduğunda hata gösteriyor

Bu değişikliğe göre artık gün için Power BI artık desteklenmektedir.

### <a name="integration-between-core-hr-and-attract"></a>Core HR ve Attract arasında tümleştirme

İlgili adayların işe alınması için Core HR ve Attract arasındaki tümleştirmeyi güncelleştirmek için bir değişiklik yapıldı. İşe alınacak adayların **Personel Yönetimi** çalışma alanında görüntülenebilir olması için aşağıdaki CDS for Apps (CDS 2.0) varlıklarının kullanılır.

İş Başvurusu
- Durum Sebebinin, Teklif Kabul Edildi olarak ayarlanması gerekir
-   Aday ve Açık Pozisyon sağlar

Aday
-   Aday bilgileri sağlar

Açık Pozisyon
-   Açık Pozisyon Kimliği ve Açık Pozisyon Katılımcıları sağlar

Açık Pozisyon Katılımcıları
-   İşe Alım Müdürü sağlar

Bir aday Personel Yönetimine eklendiğinde, aday artık aday kartında bulunan yeni seçenek kullanılarak da çıkartılabilir.

## <a name="coming-soon"></a>Çok yakında

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>İzin ve devamsızlık: Gelecekteki izin ve devamsızlık tahmini bakiyeleri

Personellerin günce izin bakiyelerini etkilemeden izin ve gelecekteki izin taleplerini tahmin etmesine olanak sağlayan değişiklikler ile görüntülenen izin bakiyeleri de değişir. 

Şu anda görüntülenen kullanılabilir bakiye tahakkukları Bugün ve onaylanan tüm ile birlikte istekleri isteklerini bırakma süresi sonuna kadar kullanılabilir kapalı süreyi aranır. 

Tahmin olanağı serbest bırakıldığı zaman, bakiye, bugünkü tahakkuklar da dahil geçerli izin bakiyesine ve bugün üzerinden taleplere değişir. Personeller ve yöneticiler bu güncelleştirilen bakiyeleri personel ve yönetici self servisinde, **İzin** kartında ve **İzin bakiyeleri** penceresinde görebilirler. İK yöneticileri, bu güncelleştirilmiş bakiyeleri **Kişiler** çalışma alanında ve personelin **Atanmış izin planları** penceresinde görebilirler.

## <a name="known-issue"></a>Bilinen sorun

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Finance and Operations ile tümleştirmede eşleşme hataları

Talent'ın Dynamics 365 for Finance and Operations ile tümleştirilmesinde geçerli şablonda aşağıdaki sorunlar belirlenmiştir. Yeni bir şablon hemen yayımlanır ve oluşturulan tüm yeni tümleştirme projelerine uygulanır. Varolan tümleştirme projeleri için görev eşleştirmeleri güncelleştirilebilir. Güncelleştirilmiş eşleşmeler için aşağıdaki tabloya bakın. 

>[!NOTE]
> İş Pozisyonları ve Pozisyonlar Ana İş Atama görevi, veri tümleştirmez. Bunun şu anda araştırması yapılmaktadır. Geçerli eşleme içinde geçici çözüm yoktur. 

İşletim birimine Departmanlar görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.

| Varolan kaynak alanı          | Yeni kaynak alanı |
| -------------------------------|------------------|
| cdm_description (Tanım)  | cdm_name (Adı)  |

Ek bir eşleşmenin de eklenmesi gerekir. Aşağıdaki eşleşmeye eklemek için son **Hiçbiri** alanını seçin.

| Kaynak alanı                   | Hedef alan    |
| -------------------------------|----------------------|
| cdm_description (Tanım)  | NAMEALIAS (NAMEALIAS)|

Güncelleştirilmiş eşlemeler aşağıdaki resimdeki gibi görünmelidir.

![İşletim birimlerine Departmanlar görevi](./media/DepartmentMapping.png)


İş Ayrıntısına İşler görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.

| Varolan kaynak alanı          | Yeni kaynak alanı                   |
| -------------------------------|------------------------------------|
| cdm_name (Adı)                | cdm_description (Tanım)      |
| cdm_name (Tanım)         | cdm_jobdescription(İş Tanımı)|


Güncelleştirilmiş eşlemeler aşağıdaki resimdeki gibi görünmelidir.

![İş Ayrıntılarına İşler görevi](./media/JobMapping.png)

İşe Çalışanlar görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.

| Varolan kaynak alanı                 | Yeni kaynak alanı                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (E-posta Adresi 1)   | cdm_primaryemailaddress (Birincil E-posta Adresi) |
| cdm_telephone1 (Telefon 1)          | cdm_primarytelephone (Birincil telefon)       |

Cinsiyet alanı dönüştürmenin de güncelleştirilmesi gerekir. **fn** (fonksiyon) eşleşme türünü Cinsiyet için seçin ve aşağıdaki değer eşleştirmelerini güncelleştirin.

| CDS değeri                   | Finance and Operations değeri                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Erkek                                             |
| 75440001                    | Kadın                                           |
| 75440002                    | Hiçbiri                                             | 
| 75440003                    | NonSpecific                                      |

Güncelleştirilmiş eşlemeler aşağıdaki resimlerdeki gibi görünmelidir.

![Çalışana Çalışanlar görevi](./media/WorkerMapping.png)

![Cinsiyet alanı dönüştürme](./media/WorkerTransform.png)
