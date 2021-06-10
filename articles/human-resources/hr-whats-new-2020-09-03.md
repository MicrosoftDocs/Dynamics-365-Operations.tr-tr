---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (03 Eylül 2020)
description: Bu konuda, 3 Eylül 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c8ad853b8d1f8383b23f2ac4341a5f37a904795
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054464"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (3 Eylül 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3504 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

Human Resources uygulamasında yakında sunulacak özellikler hakkında daha fazla bilgi için, bkz. [Dynamics 365 Human Resources 2019 Sürüm Dalga 2'ye Genel Bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Human Resources güncelleştirme işlemi hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Bu sürümde

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Human Resources uygulamasının tamamında yeni varsayılan mali boyutlar kılavuz ve iletişim düzeni (469495)

Mali boyutların yeni modeli artık aşağıdaki alanlarda kullanılabilir:

- Pozisyon eylemleri (form: **HcmPositionActionDetail**)
- Bordro kazanç kodları (Form: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>İzin ve devamsızlık takvim geliştirmeleri etkinleştirilmemişse, girişler şirket izin takviminde görünmez (484406)

Bu sürümde, izin girişlerinin şirket izin takviminde gösterilmemesi ile ilgili sorun düzeltilmiştir. Bu sorun yalnızca Özellik yönetimi seçeneği **İzin ve devamsızlık takvimi geliştirmeleri** etkinleştirilmemişse ortaya çıkar.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity sorunu (467597)

Bu sürümde, **BenefitsPlanEmployee** varlığındaki bir sorun düzeltilmiştir. Çalışan kayıt anlaşmaları içeri aktarılırken **Kapsam kodu** ve **Plan türü kodu** artık doğru şekilde ayarlanıyor. Bu sorun, personel kazanç planlarının Personel self servisi'ndeki **Çalışan kazanç planları** ve **Açık kayıt anlaşması** formlarında yanlış gösterilmesine neden oluyordu.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>XML'de elektronik dosya 1094-C çıktı eksik harfi (435190)

Bu değişiklik, IRS'ye gönderim sırasında gerekli olan eksik bir karakterin bulunduğu1094-C çıktı dosyası ile ilgili bir sorunu düzeltmiştir.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Sabit maaş formu ile eşlenen çalışan değişken maaş tablosu (476117)

Bu değişiklik sabit maaş alanlarını sabit maaş formu ile hizalar. Değişken maaş alanları artık yalnızca değişken maaş formu ile kullanılabilir.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>İzin tipinde negatif minimum bakiye varsa, kayıt öncesinde izin verilen bu izin istekleri (469917)

Bu değişiklik, kayıt negatif bir minimum bakiyeye sahip olsa bile, plana kaydolmadan önce izin taleplerini girmeyi engeller. Yalnızca plan etkinken talep girebilir veya gönderebilirsiniz.

### <a name="document-templates-dont-download-457279"></a>Belge şablonları indirilmiyor (457279)

Bu değişiklikle artık tüm belge şablonlarını indirebilirsiniz. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Veriler, ücret planı raporunda Ödeme oranı alanına ait satırlar yerine sütun başlıkları olarak görüntülenir (476077)

Analiz raporu artık **Ödeme oranı** hakkında doğru bilgileri görüntüler.

## <a name="in-preview"></a>Ön izlemede

### <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources belgelerinde [Teams içinde Human Resources uygulaması](./hr-admin-teams-leave-app.md)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams'de Human Resources uygulaması önizleme özellikleri
 
-  **Bildirimler**: Teams'deki Human Resources uygulamasında izin isteklerini gönderen ve onaylayan kişiler bildirim alacak. Onaylayanlar, izin isteklerini onaylayabilir veya reddedebilir. Göndericiler, istek onaylandıysa veya reddedilmişse bilgilendirilir. Daha fazla bilgi için bkz:
   - Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources belgelerinde [Teams içinde Human Resources uygulamasına ait bildirimleri etkinleştirme](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)
   - Human Resources belgelerinde [Tek tek kullanıcılar için Teams bildirimlerini açma veya kapatma](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)
   - Human Resources belgelerinde [Teams Bildirimleri](./hr-teams-leave-app.md#respond-to-teams-notifications)
   - Human Resources belgelerinde [Takımınızın takvimini görüntüleme](./hr-teams-leave-app.md#view-your-teams-leave-calendar)
 
- **Yönetici izin takvimi**: Yöneticiler, doğrudan onlara bağlı çalışanlar için onaylanan ve bekleyen izinleri takvim görünümünde görebilecek. Bu görünüm, takım üyelerinin izinde olduğu tarihlerin daha kolay anlaşılmasını sağlar. Daha fazla bilgi için bkz:
   - Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources belgelerinde [Takımınızın takvimini görüntüleme](./hr-teams-leave-app.md#view-your-teams-leave-calendar)

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği (477004)

Panonun sağ sütunundaki **Bana atanan çalışma öğeleri** listesini konumlandırmak için yeni bir seçenek bulunur. Bu değişiklikle, tüm çalışma öğeleri ve yapılacak işler listeleri aynı alanda görüntülenebilir. Özellik yönetiminde **Önizleme: İş akışı deneyimi geliştirmeleri** özelliğini etkinleştirerek bu işlevi etkinleştirin. Önizleme özelliklerini açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

Bu özellik ayrıca, personel eylemleri formlarında görünen iş akışı seçeneklerini de yükseltir. Ayrıca, hızlı erişim için eylem hızlı sekmesinin üstünde iş akışı seçenekleri de görüntülenir. Daha fazla bilgi için bkz: 

- Dynamics 365 2020 sürüm dalga 2 planında [Kuruluş ve personel yönetimi iş akışı deneyimi iyileştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)

![Bana atanan iş öğeleri](./media/hr-workflow-work-items-assigned-to-me.png)

![İş akışı öğelerine hızlı erişim](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Çok Yakında

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

### <a name="benefits-management-reason-codes"></a>Yan haklar yönetimi neden kodları

Yan haklar yönetimi neden kodları Human Resources içinde var olan neden kodlarıyla yakında birleştirilecektir. Yan haklar yönetiminde 15 karakterden uzun neden kodları oluşturduysanız, Yan haklar yönetimi **Neden kodları** formunda neden kodunun adını 15 karakter veya daha az olacak şekilde değiştirmeniz gerekir. Adı güncelleştirdiğinizde, neden kodu, Personel yönetimi'nde var olan neden kodu formunun altında görüntülenir. Bu değişiklik gelecekte kullanılabilir olacak ve var olan işlevleri etkilemeyecek.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
