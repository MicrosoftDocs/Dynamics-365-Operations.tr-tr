---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler, 22 Haziran 2021
description: Bu konuda, 22 Haziran 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae444b4d208804364333bd3d6e4704500da85470
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303574"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler, 22 Haziran 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4258 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kullanıcıları istihdamı olmayan çalışanlar hakkında bilgilendir özelliği: Gelişmiş erişim açık olduğunda **İstihdamı olmayan çalışanların tümünü görüntüle** özelliği özellik yönetiminde devre dışı bırakıldığında, istihdamı olmayan çalışanlar formunda bir başlık görüntülenir. Başlık, kullanıcıyı **İstihdamı olmayan tüm çalışanları görüntüle** özelliğini açmaya yönlendirir. | Geçerli değil| [İstihdamı bulunmayan çalışanlar](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Kazançlar yönetimi uygunluğu kurallarında özel alanlar desteği | [Uygunluk işleme için özel alan desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Uygunluk kurallarını yapılandırma](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| İzin tahakkuku hareketi denetleme | Geçerli değil | [İzin tahakkuku hareketi denetleme](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|
| İzin ve devamsızlık iş akışı deneyiminde geliştirmeler | [İzin ve devamsızlık iş akışı deneyiminde geliştirmeler](https://go.microsoft.com/fwlink/?linkid=2147528) | [İzin iste](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun |  Tanım |
| --- | --- | --- |
| 583052 | Geri bildirim alan kullanıcı alınan geri bildirimi düzenleyebilir | Performans günlüğünde geri bildirim alan bir çalışan **Harici bağlantı ekle**'yi seçerse, form düzenlenebilir hale gelir ve çalışanın aldığı performans geri bildirimini düzenlemesine olanak sağlar. |
| 522281 | Ücret Yönetimindeki ücret yapısı kutucuklarında çalışan sayısını seçme yanlış sonuçlara neden oluyor| Ücret çalışma alanından ücret planı ayrıtnılarına gidildiğinde, artık doğru çalışan sayısı görüntüleniyor. |
| 580683 | Çalışan ve Yönetici rollerine atanan kullanıcılar not ekleyemiyor veya Performans günlüğünü güncelleştiremiyor | Çalışan ve Yönetici rollerine atanan kullanıcılar not ekleyemiyor veya Performans günlüğünü güncelleştiremiyor. Kullanıcı "Performans günlüğü girişinde bir kayıt oluşturulamıyor (HcmPerfJournal). Güvenlik ilkesi izni verilmedi." hatasını alıyor |
| 583077 | İzin ve devamsızlık şirketi takviminde bir çalışanın doğum günü tarihi yanlış bir tarih gösteriyor | Kullanıcılar, izin ve devamsızlık şirket takviminde çalışanların doğru doğum tarihini görüntüleyebilirler. |
| 586996 | Şirketler arası izin görünümü özelliği tek bir şirketle erişim kısıtlanmışsa bakiyelerin boş olmasına neden oluyor | Şirketler arası izin görünümü etkinleştirildiğinde, kullanıcılar çalışanın gelecekteki izin bakiyesini doğru olarak görüntüleyebilir. |
| 581014 | Şirketler arası izin ve devamsızlık görünümünü etkinleştirmek gelecekteki bakiyeleri görüntülerken bir hataya neden oluyor | Kullanıcılar şirketler arası izin görünümüyle gelecekteki izin bakiyelerini görüntüledikleri sırada oluşan hatalar düzeltildi. |
| 509404 | Departman Kişi sayısı analizi, çalışanların departmanlar arasındaki hareketini dikkate almaz. | Bir çalışan bir departmandan diğerine geçtiğinde, departman sayısı verileri, pozisyon ayrıntısı geçerli yıl içinde sona erdiyse, çalışanın geldiği eski departmanı yansıtmaz. |
| 584851 | Kazanç alacağını eşit dağıtma kuralı "Hiçbiri" kesinlikle alacak sağlamıyor |Esnek alacak eşit dağıtma kuralı "Hiçbiri" işe alınma tarihleri ne olursa olsun, çalışanların kazanç dönemi için sıfır alacak almalarına neden oldu. Bu, çalışanın kazanç süresi başlamadan önce işe alınmış olması durumunda tüm esnek alacakları almasını ve dönem başladıktan sonra işe alınması durumunda hiçbirini almamasını sağlayacak şekilde düzeltildi. |
| 584897 | 'Temel harici işlevselliği kullan' görevlerinin çoğaltılması hata ile sonuçlanıyor | 'Temel harici işlevselliği kullan' görevini yinelemeye çalışılırken kullanıcı "UserDefinedAppHostDialogView tanmlayıcısına sahip bir nesne bulunamadı" hatasını alıyordu. |
| 575692 | İzin ve devamsızlık tahakkuku bekleyen çalışanlar için kullanılamıyor | **Kolaylaştırılmış çalışan girişi** etkinleştirildiğinde, izin ve devamsızlık tahakkuku gelecekteki işe alımlarda çalıştırılabilir. |
| 580110 | Bir şirketi Bordro tümleştirmesine eklemek, seçenek projeyi yenileme olarak ayarlanmış olsa bile tümleştirmeyi tüm varlıkları kullanacak şekilde sıfırlıyor | Müşteri, bordro tümleştirmesi için varlıkları kaldırmış veya veri projesini değitirmişse ve projenin otomatik yenilenmesini önleyebilecek seçenek kümesine sahipse, tümleştirmeye yeni bir şirket eklemek ayarı yoksayar ve projeyi yeniler.  |
| 584518 |Kazanç kayıtlarını işleme performansı sorunu | Bu hata, eski kazanç kaydı sürecindeki performans sorunlarını gidermeye yöneliktir. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Platform güncelleştirmesi 10.0.19 (43) | Platform Update 10.0.19, 28 Haziran 2021'deki hizmet sürümü ile kullanıma sunulmak üzere zamanlanmıştır. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.19 sürümü için platform güncelleştirmeleri (Haziran 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Hizmet yılı görüntüleme geçişi | Bu özellik, **Kolaylaştırılmış çalışan girişi** formunda ve **Kişiler** formunda görüntülenen hizmet yılların hesaplanması için farklı tarihler kullanma seçeneği sağlar.  Bu, Human Resources parametrelerinde kullanılabilir olacaktır. |
|  Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Belirli izin türleri için ekleri zorunlu kılma | Bu özellik, yöneticilerin belirli izin türlerinde izin istekleri gönderilirken eklerin iliştirilmesini zorunlu tutmalarını sağlar. |
|  İzin birimlerini izin türüne göre yapılandır | Bu özellik, yöneticilerin her izin türü için izin birimlerini (saatler veya günler) yapılandırmasını sağlar.  |
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
