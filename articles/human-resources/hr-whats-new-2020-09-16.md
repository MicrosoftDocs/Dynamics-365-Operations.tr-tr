---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (16 Eylül 2020)
description: Bu konuda, 16 Eylül 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14a4c08b0d223bc7fd8044354f5976388af9176b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467469"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (16 Eylül 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3557 uygulanır. Bazı özelliklerin yanında bulunan parantez içindeki numaralar Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="included-in-this-release"></a>Bu sürümdeki içerik

-  [Kayıtlı görünümler - genel kullanılabilirlik](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Daha fazla bilgi için, bkz. [Kayıtlı görünümler](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- **Pozisyon eylemleri** formunda güncelleştirilmiş bir boyut kılavuzu ve yeni iletişim kutusu (469495) vardır.

- **Human Resources Paylaşılan parametreler**'e **Gelişmiş erişim**'de **Çalışan bilgilerine erişimi kısıtlamak** ayarını evet olarak ayarlarsanız, yan haklar formları artık yalnızca uygun çalışanları gösterir (393384).

- **WorkCalendar** varlığında yeni takvim oluşturma seçenekleri (477055):<br>- Varsayılan bitiş zamanı<br>- Varsayılan başlangıç zamanı<br>- Cuma çalışma günüdür<br>- Pazartesi çalışma günüdür<br>- Cumartesi çalışma günüdür<br>- Pazar çalışma günüdür<br>- Perşembe çalışma günüdür<br>- Salı çalışma günüdür<br>- Çarşamba çalışma günüdür<br>- İş Takvimi tatil kodu

- **LeaveBankTransactionV1** varlığı şimdi neden kodunu içerir (477823).

- Artık görev kayıtlarını kaydedebilirsiniz (492923).

- Veriler artık **HCMWorkerContactEntity** öğesinden başarıyla yayımlandı (427620).

- **Ücret** hızlı sekmesi artık yüklenici çalışan türü için **Çalışan eylemleri** formunda görüntülenir (482494).

- Artık **Sabit ücret** ayarladıysanız, **Düzey** ve **Plan** alanları zorunludur. Bu alanları boş bırakırsanız hata iletisi görüntülenir (482497).

- **Kazanç** ögesinde **Plan türü** alanı artık bir açılır listedir (488768).

- Human Resources'dan bir özel alan silinirse sistem yöneticileri artık bildirim almaya başlar (481408).

- Çalışanın işine son verme işlemi sırasında, Human Resources beklendiği gibi davranır ve kilitleme olarak görüntülendikten sonra seçili şirketi değiştirmez (479877). 

- Yöneticiler artık kişiselleştirme yoluyla bir numara sütunu ekleyemez (485317).

- Yöneticiler, artık süresi dolan kimlik numaralarından veri aralığı filtresini kaldıramazlar (485321).

- **Bağlı olduğu kişi** alanı boş olduğunda pozisyon ayrıntıları pozisyon üzerine imleç getirildiğinde görüntülenmeye devam eder (433328).

- Çalışanlar artık, Employee self service'de kazanç planı bilgilerini görüntüleyebilir (481676).

- Çalışanlar artık tüm kayıtlı kursları görebilir (429048).

- Artık **Profesyonel sertifikalar** sayfası için görüntüleme seçeneklerini kısıtlayabilirsiniz. Görüntüleme seçeneklerini geçerli yasal varlığa, çalışan durumuna göre ve çalışan türüne göre kısıtlayabilirsiniz (451501). 


## <a name="in-preview"></a>Ön izlemede

### <a name="human-resources-app-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources belgelerinde [Teams içinde Human Resources uygulaması](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams'de Human Resources uygulaması önizleme özellikleri
 
-  **Bildirimler**: Teams'deki Human Resources uygulamasında izin isteklerini gönderen ve onaylayan kişiler bildirim alacak. Onaylayanlar, izin isteklerini onaylayabilir veya reddedebilir. Göndericiler, istek onaylandıysa veya reddedilmişse bilgilendirilir. Daha fazla bilgi için bkz:
   - Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources belgelerinde [Teams içinde Human Resources uygulamasına ait bildirimleri etkinleştirme](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams)
   - Human Resources belgelerinde [Tek tek kullanıcılar için Teams bildirimlerini açma veya kapatma](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users)
   - Human Resources belgelerinde [Teams Bildirimleri](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications)
   - Human Resources belgelerinde [Takımınızın takvimini görüntüleme](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)
 
- **Yönetici izin takvimi**: Yöneticiler, doğrudan onlara bağlı çalışanlar için onaylanan ve bekleyen izinleri takvim görünümünde görebilir. Bu görünüm, takım üyelerinin izinde olduğu tarihlerin daha kolay anlaşılmasını sağlar. Daha fazla bilgi için bkz:
   - Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources belgelerinde [Takımınızın takvimini görüntüleme](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği (477004)

Panonun sağ sütunundaki **Bana atanan çalışma öğeleri** listesini konumlandırmak için yeni bir seçenek bulunur. Bu değişiklikle, tüm çalışma öğeleri ve yapılacak işler listeleri aynı alanda görüntülenebilir. Özellik yönetiminde **Önizleme: İş akışı deneyimi geliştirmeleri** özelliğini etkinleştirerek bu işlevi etkinleştirin. Önizleme özelliklerini açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

Bu özellik ayrıca, personel eylemleri formlarında görünen iş akışı seçeneklerini de yükseltir. Ayrıca, hızlı erişim için eylem hızlı sekmesinin üstünde iş akışı seçenekleri de görüntülenir. Daha fazla bilgi için bkz: 

- Dynamics 365 2020 sürüm dalga 2 planında [Kuruluş ve personel yönetimi iş akışı deneyimi iyileştirmeleri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)

![Bana atanan iş öğeleri](./media/hr-workflow-work-items-assigned-to-me.png)

![İş akışı öğelerine hızlı erişim](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>İzin ve devamsızlık takvimi

Bu sürüm, izin ve devamsızlık takvimleri için ek takvim seçenekleri içerir. Daha fazla bilgi için bkz. [Ekip ve şirket takvimlerini görüntüleyin](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Çok Yakında

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

### <a name="benefits-management-reason-codes"></a>Yan haklar yönetimi neden kodları

Yan haklar yönetimi neden kodları Human Resources içinde var olan neden kodlarıyla yakında birleştirilecektir. Yan haklar yönetiminde 15 karakterden uzun neden kodları oluşturduysanız, Yan haklar yönetimi **Neden kodları** formunda neden kodunun adını 15 karakter veya daha az olacak şekilde değiştirmeniz gerekir. Adı güncelleştirdiğinizde, neden kodu, Personel yönetimi'nde var olan neden kodu formunun altında görüntülenir. Bu değişiklik gelecekte kullanılabilir olacaktır ve var olan işlevleri etkilemeyecek.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]