---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (6 Aralık 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e46000414436b5a2fa211428dcd10131b9d588c1
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897707"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (6 Aralık 2018)

**Derleme 8.1.2071**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.


## <a name="platform-update-22-for-finance-and-operations"></a>Finance and Operations için platform güncelleştirmesi 22

### <a name="export-up-to-1-million-rows-to-excel"></a>Excel'e 1 milyon satıra kadar aktarın

Excel'e aktar özelliği artık kullanıcıların 1 milyona kadar satırı Talent içindeki bir kılavuzdan aktarmasına izin verir; bu da önceki 10.000 satır sınırına göre ciddi bir artıştır. 

### <a name="restyled-personalization-toolbar"></a>Yeniden şekillendirilmiş kişiselleştirme araç çubuğu

Kişiselleştirme araç çubuğu, Finance and Operations için Platform Güncelleştirmesi 22'de kullanıcıların Talent'ta kendi deneyimlerini daha kolay özelleştirmelerine yardımcı olmak için yeniden şekillendirilmiştir. Şu değişiklikler yapılmıştır: 

-  Kullanıcıların kullanmakla ilgilendikleri aracı daha hızlı tanımaları için her kişiselleştirme aracı artık bir simgeyle gösterilmektedir.
-  Geçerli aracın nasıl kullanılacağının açıklaması da artık gösterilir, bu da kullanıcıların ihtiyaç duyulan kişiselleştirmeyi nasıl yapacaklarını anlamalarını sağlar.  
-  Tüm kişiselleştirme araç çubuğu, sol araç çubuğunun belirli bir yerine sürüklenip bırakılmak şeklinde taşınabilmektedir. Bu, kullanıcıların daha önce araç çubuğu tarafından kapatılan öğeleri kişiselleştirmesine olanak tanır.   

### <a name="optimized-is-one-of-filtering-experience"></a>İyileştirilmiş, "biri" filtreleme deneyimini en iyi duruma getirir

"Biri" filtreleme operatörü, Filtre Panosu ve kılavuz başlık açılır listesi kullanırken çoğu alan için kullanılabilirdir. Bu işleç, kullanıcının birden fazla değerlerini temel alan bir alana filtrelemesine izin verir. Bu, Finance and Operations için Platform güncelleştirmesi 22'de, "biri" işleci için yeni ve geliştirilmiş bir deneyim kullanıma sunulmuştur. Daha fazla bilgi için bkz. [En iyi duruma getirilen "biri" filtreleme deneyimi](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>"Biri" operatörü ile listeleri Excel'den filtre alanlarına yapıştırın

Bazı görevler için kullanıcıların Talent içinde veri filtrelemek için kullanmak isteyecekleri bir değerler listesi olabilir. Örneğin, bir İnsan Kaynakları kullanıcısı, çalışanlar sistemde ek araştırma gerektiren bir rapordaki bir dizi tanımlanmış ve doğrudan Excel'den beceri Filtresi alanına listeyi kopyalamak bu kullanıcı için en uygun.

Finance and Operations için Platform güncelleştirmesi 22 ile başlayarak, Filtre Bölmesindeki "biri" işleci ve kılavuz sütun filtreleme artık Excel'den kopyalanan listeleri tanıyor ve böylece doğrudan bir filtre alanına yapıştırılabiliyor. Bu, Excel'deki farklı satır ve sütunlardan kopyalanan bir dizi değeri içerir. Bu özellik hakkında daha fazla bilgi için bkz: ["Biri" operatörü ile filtre alanlarına Excel'den liste yapıştırın](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>Ön izlemede

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>Talent ve Dayforce arasında UK bordro tümleştirmeyi yapılandırma

Talent ve Ceridian Dayforce arasındaki tümleştirme Birleşik Krallık'ta önizlemeye açılmıştır. Daha fazla bilgi için aşağıdaki konuya bakın: [Talent ve Dayforce arasındaki bordro tümleştirmesini yapılandırma](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Çok yakında

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>İzin ve devamsızlık: Gelecekteki izin ve devamsızlık tahmini bakiyeleri

Personellerin günce izin bakiyelerini etkilemeden izin ve gelecekteki izin taleplerini tahmin etmesine olanak sağlayan değişiklikler ile görüntülenen izin bakiyeleri de değişir. 

Şu anda görüntülenen kullanılabilir bakiye tahakkukları Bugün ve onaylanan tüm ile birlikte istekleri isteklerini bırakma süresi sonuna kadar kullanılabilir kapalı süreyi aranır. 

Tahmin olanağı serbest bırakıldığı zaman, bakiye, bugünkü tahakkuklar da dahil geçerli izin bakiyesine ve bugün üzerinden taleplere değişir. Personeller ve yöneticiler bu güncelleştirilen bakiyeleri personel ve yönetici self servisinde, **İzin** kartında ve **İzin bakiyeleri** penceresinde görebilirler. İK yöneticileri, bu güncelleştirilmiş bakiyeleri **Kişiler** çalışma alanında ve personelin **Atanmış izin planları** penceresinde görebilirler.

## <a name="other-changes"></a>Diğer değişimler 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>İşe son verme kodu, çalışan pozisyon atama kaydında doldurulmamıştır

Pozisyon atama kaydında işe son verme işlemi sırasında neden kodunu dolduran bir değişiklik uygulanmıştır.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Kullanımdaki personel numarası için doğrulamanın ek ayrıntılara ihtiyacı vardır

Ek bilgi, numara serileri kullanımda olduğunda görüntülenir, bu sayede yeni bir numara oluşturulamadığında nedenler daha iyi anlaşılır.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Eklenti düğmeleri çalışanlar için kullanılabilir değildir

Ekleri düzeltmek için değişiklikler yapılmıştır. Bir çalışana yeni bir ek eklendiğinde, **Yeni** ve **Düzenle** düğmeleri artık FactBoxes çalışan penceresinde açık olduğunda kullanılabilirdir. 

## <a name="known-issues"></a>Bilinen sorunlar

### <a name="mapping-errors-in-the-integration-with-finance"></a>Finance ile tümleştirmede eşleşme hataları

Talent'ın Finance ile tümleştirilmesi için kullanılmakta olan şablonda aşağıdaki sorunlar belirlenmiştir. Yeni bir şablon hemen yayımlanır ve oluşturulan tüm yeni tümleştirme projelerine uygulanır. Varolan tümleştirme projeleri için görev eşleştirmeleri güncelleştirilebilir. Güncelleştirilmiş eşleşmeler için aşağıdaki tabloya bakın. 

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

Güncelleştirilmiş eşlemeler şu şekilde görünmelidir.

![İşletim birimlerine Departmanlar görevi](./media/DepartmentMapping.png)


İş Ayrıntısına İşler görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.

| Varolan kaynak alanı          | Yeni kaynak alanı                   |
| -------------------------------|------------------------------------|
| cdm_name (Adı)                | cdm_description (Tanım)      |
| cdm_name (Tanım)         | cdm_jobdescription(İş Tanımı)|


Güncelleştirilmiş eşlemeler şu şekilde görünmelidir.

![İş Ayrıntılarına İşler görevi](./media/JobMapping.png)

İşe Çalışanlar görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.

| Varolan kaynak alanı                 | Yeni kaynak alanı                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (E-posta Adresi 1)   | cdm_primaryemailaddress (Birincil E-posta Adresi) |
| cdm_telephone1 (Telefon 1)          | cdm_primarytelephone (Birincil telefon)       |

Cinsiyet alanı dönüştürmenin de güncelleştirilmesi gerekir. **fn** (fonksiyon) eşleşme türünü Cinsiyet için seçin ve aşağıdaki değer eşleştirmelerini güncelleştirin.

| Common Data Service Değeri   | Finance and Operations değeri | | ------------|------------------ -----------| | 75440000    | Erkek                         | | 75440001    | Kadın                       | | 75440002    | Yok                         | | 75440003    | NonSpecific                  |

Güncelleştirilmiş eşlemeler şu şekilde görünmelidir.

![Çalışana Çalışanlar görevi](./media/WorkerMapping.png)

![Cinsiyet alanı dönüştürme](./media/WorkerTransform.png)

