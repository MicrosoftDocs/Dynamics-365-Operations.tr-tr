---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (3 Nisan 2020)
description: Bu makalede, Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab732853a2c37338d8003c5f8911c011aa8ffc60
ms.sourcegitcommit: 724f5b400a4e7c385da9d8b22db416ebc3623b93
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/03/2020
ms.locfileid: "3225163"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (3 Nisan 2020)

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3111 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>6 Nisan haftasında genel kullanıma sunulan özellikler

- **İzin ve devamsızlık özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md).

- **Kazanç yönetimi özellikleri** - Daha fazla bilgi için bkz. [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>İnsan Kaynakları ortam sınırları Şimdi güncelleştirilmiş lisansa dayalıdır (394595)

LCS içindeki proje başına ortam sayısı sınırı değişti. Önceki sınır iki ortamlıda. LCS içindeki İnsan Kaynakları için oluşturabileceğiniz üretim ve korumalı alan ortamlarının sayısı sınırı Şimdi güncelleştirilmiş lisansa dayalıdır. Artık tüm LCS projesi başına gereken sayıda ortam satın alınan lisans sayısına bağlı olarak oluşturabilirsiniz. 1 Şubat 2020 tarihinde güncelleştirilen yeni lisans müşterilerin ek ortamlar satın almanıza olanak tanır. Ek ortamların lisans gereksinimleri hakkında daha fazla bilgi için bkz. [Dynamics 365 lisans Kılavuzu](https://dynamics.microsoft.com/pricing/#HumanResources)'na bakın.
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Soru formu silinmeye çalışılırken hata (428603)

Bu haftanın güncelleştirmesi, bir soru formunu silmeye çalışırken aşağıdaki hata nedeniyle görüntülenen bir sorunu düzeltir:

Dengesiz bir X++ TTSBEGIN/TTSCOMMIT çifti algılandı.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Performans günlüğü ve profesyonel sertifika güvenlik sorunu (428499)

Bu değişiklik, erişim izni olan şirketleri temel alarak performans günlüklerinin ve profesyonel sertifikaların görünürlüğünü sınırlar. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Quebec ve Manitoba kısaltması (387510)

Başlangıç verileri, Manitoba ve Quebec için doğru kısaltmayı yansıtacak şekilde güncelleştirilmiştir.

## <a name="new-entities-available-in-data-management-framework"></a>Yeni varlıklar Veri Yönetim Çerçevesinde bulunur

Aşağıdaki varlıklar artık kullanılabilir. Varlıklar listesinde bu varlıkları listelenmiş olarak göremezseniz, **Çerçeve Parametreleri > VArlık ayarları > Varlık listesini yenile**'deki **Varlıkları yenile** seçeneğini kullanın.

 - İzin ve devamsızlık banka hareketi V2
 - İzin ve devamsızlık kaydı V2
 - İzin ve devamsızlık planı katmanı V2
 - İzin ve devamsızlık planı V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service çözümü şimdi aşağıdaki değişikliklerle kullanılabilir:

| Tanım | Değiştirme |
| --- | --- |
| **İş/pozisyon** varlığı değişiklikleri | <ul><li>**Ücret bölgesi** eklendi</li>|
| **İş pozisyonu boyutu** varlığı eklendi | <ul><li>**Mali boyutlar** eklende</li>
| **Çalışan varlığı** değişiklikleri | <ul><li>**Ad sırası** eklendi</li><li>**Evden çalışma** eklendi</li><li>**Dil** eklendi</li><li>**Kıdem tarihi** eklendi</li><li>**Yıldönümü tarihi** eklendi</li><li>**Orijinal işe alma tarihi** eklendi</li></ul> |
| **İstihdam** varlık değişiklikleri | <ul><li>**Mali boyutlar** eklende</li><li>**İşten çıkarma nedeni** eklendi</li><li>**Geçiş tarihinden** yeniden adlandırılan **sonlandırma tarihi**</li><li>**Deneme tarihleri** eklendi</li></ul> |
| **Çalışan adresi** varlık değişiklikleri | <ul><li>**Cadde Adresi** eklendi</li><li>**Adres satırı 1**, **Adres satırı 2** ve **Adres satırı 3** itiraz için işaretlenmiş.</li></ul> |
| Yeni değişken ücret kurulumu varlıkları | <ul><li>**Değişken Ücret Planı Türü**</li><li>**Maaş değişken planı**</li><li>**Hakediş ödeme kuralları**</li><li>**Değişken Ücret Planı Düzeyi**</li></ul> |
| Yeni **çalışan takvimi çalışan** varlığı | <ul><li>**İş takvimi varlığı** eklendi</li></ul> |
| Yeni **Bordro pozisyon ayrıntısı** varlığı | <ul><li>**Bordro pozisyon ayrıntısı** eklendi</li></ul> |
| Yeni **Başlık** varlığı | <ul><li>**Unvan** eklendi</li></ul>Common Data Service'a yeni **Unvan** varlığı eklendi ancak bu varlığa şu an için  **İş Pozisyonu** veya **İş** varlıklarından başvurulamamaktadır. |

> [!NOTE]
> Pozisyonlar ve istihdam için mali boyutlar, Human Resources'tan Common Data Service'a güncelleştirmeler için tek yönlü tümleştirme sağlar. Mali boyut güncelleştirmeleri şu an için Common Data Service'tan Human Resources ile eşitlenmez.

Gelecek birkaç hafta içinde bu varlık değişiklikleri tüm ortamlarda kullanılabilir olacaktır. Human Resources için en son Common Data Service çözümünü el ile yüklemek için:

1.  [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ne gidin.

2.  **Ortamlar**'ı seçin.

3.  Yükseltmek istediğiniz ortamı bulun. Ortam, Human Resources'taki **Hakkında** formunun **Common Data Service bilgileri** bölümündeki **Ortam adı**'na karşılık gelmelidir.

4.  Ortam ayrıntılarını görüntülemek için ortamı seçin.

5.  Üstteki eylem çubuğunda **Çözümleri Yönet**'i seçin. Yeni bir tarayıcı penceresi açılır ve ortamınızın bağlamında **Dynamics 365 Yönetim Merkezi**'ne gider.

6.  **Çözüm** listesinde, **Dynamics 365 Human Resources Bağlayıcısını** seçin.

7.  En son çözümü uygulamak için **Yükselt**'i seçin.

## <a name="in-preview"></a>Ön izlemede

## <a name="leave-suspension"></a>İzni askıya alma

Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Devretme kuralları

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Çok Yakında

## <a name="new-production-release-cadence"></a>Yeni üretim sürümü temposu

Nisan ayından başlayarak, Human Resources sürüm temposu bir haftalık güncelleştirme yerine iki haftalık güncelleştirme olacak şekilde değiştirilecektir. Güvenli dağıtım uygulamalarıyla uyumu sağlamak ve hizmette yüksek kararlılık ve güvenilirlik standartlarını korumak için, tüm bölgelere hizmet güncelleştirmelerini dağıtma işlemi iki haftalık bir dağıtım olacaktır. İşlemin her aşamasında başarılı dağıtımı doğrulamak için ek test ve izleyiciler olacaktır. Sürüm temposu hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Bilinen sorunlar

## <a name="employment-detail-entity"></a>İstihdam Ayrıntısı varlığı

**İstihdam Ayrıntısı** varlığı aşağıdaki alanlarla güncelleştirildi: **PayFrequency**, **İstihdam Kategorisi Kodu**, **İstihdam Türü**, **EmploymentType Kodu** ve **Kazanç İstihdam Durumu**. Bu alanların kurulum verileri, Özellik yönetiminde etkinleştirilen kazanç yönetimine bağlıdır. İçe aktarma sırasında hatalara neden olacağından, bu alanlar **İstihdam Ayrıntısı** varlığında doldurulmamalı veya güncelleştirilmemelidir.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint Önizleme bazı ortamlarda çalışmıyor

SharePoint'te depolanan belgelere ait belge önizlemesi çalışmazsa, aşağıdaki yordamı deneyin:

1. Yönetici Kullanıcı hesabının kullanıcı kaydıyla ilişkili bir e-posta olduğunu doğrulayın. Bu bilgileri **Kullanıcı** sayfasında görüntüleyebilirsiniz. E-posta ayarlanmamışsa, OData Excel eklentisi ile e-posta ve sağlayıcı eklemeniz gerekir. Varsayılan olarak, e-posta adresi Excel tasarımında bulunmaz. Excel tasarımını düzenlemeniz, tüm alanları eklemeniz, uygulamanız ve yenilemeniz gerekir. Bu adımları tamamladıktan sonra, yönetici hesabını güncelleştirebilirsiniz.

2. Yönetici hesabının ilişkili bir e-posta hesabı varsa, yönetici kimlik bilgileriyle İnsan Kaynakları için oturum açın.

3. Belge önizlemesini başlatmak için SharePoint ' deki bir eke erişin.

4. Eklere erişimi olan başka bir kullanıcı hesabıyla oturum açın ve önizlemenin beklendiği gibi çalıştığını doğrulayın.