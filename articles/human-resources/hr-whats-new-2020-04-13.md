---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (13 Nisan 2020)
description: Bu makalede, 13 Nisan 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9219e3f2da4d398ed7e8bb27337835d42403925
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692821"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (13 Nisan 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3136 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="new-production-release-cadence"></a>Yeni üretim sürümü temposu

Bu haftanın sürümüyle, Human Resources sürüm temposu bir haftalık güncelleştirmeden iki haftada bir güncelleştirme olacak şekilde değişecektir. Güvenli dağıtım uygulamalarıyla uyumu sağlamak ve hizmette yüksek kararlılık ve güvenilirlik standartlarını korumak için, tüm bölgelere hizmet güncelleştirmelerini dağıtma işlemi artık iki haftalık bir dağıtım olacaktır. İşlemin her aşamasında başarılı dağıtımı doğrulamak için ek test ve izleyiciler bulunur. Sürüm temposu hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Yuvarlama hassasiyeti alanı bir Yuvarlama türü belirttikten sonra düzenlenemez (435616)

Bu değişiklikle, **Yuvarlama hassasiyeti** alanı şimdi **Yuvarlama türü** alanını güncelleştirdikten sonra kullanılabilir.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>İzin planı tahakkuk dönemi içermiyorsa, izin kaydı bitiş tarihi düzenlenemiyor (413628)

Artık kayıt bitiş tarihini, "Alan tahakkuk tarihi esası doldurulmalıdır" hatasını almadan düzenleyebilirsiniz.

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>İstihdam varlığı Dataverse ile eşitlenmiyor (430834)

Bu değişiklik, mali boyutlar eklendikten sonra istihdam verilerinin Dataverse eşitlenmemesine yol açan bir sorunu düzeltir. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>İş Takvimi Zaman Aralığı varlığı için birden çok üst düzeyi kaldır (431775)

Bu değişiklik, **İş Takvimi Zaman Aralığı** varlığı için birden çok üst düzeyi kaldırır.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>CAST işlevi ile filtre uygulama OData çağrısı Pozisyona Çalışan Atama varlığı üzerinde çalışmıyor (431699)

Bu güncelleştirme, OData içindeki CAST işlevine **Pozisyon Çalışan Ataması** varlığı filtre uygulama izni veren bir değişiklik içerir.

## <a name="in-preview"></a>Ön izlemede

## <a name="leave-suspension"></a>İzni askıya alma

Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Devretme kuralları

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Bilinen sorunlar

## <a name="employment-details-entity"></a>İstihdam Ayrıntıları varlığı

**İstihdam Ayrıntısı** varlığı aşağıdaki alanlarla güncelleştirildi:

- **PayFrequency**
- **İstihdam Kategorisi Kodu**
- **İstihdam Türü**
- **EmploymentType Kodu**
- **Kazanç İstihdam Durumu**

Bu alanların kurulum verileri, **Özellik yönetimi** çalışma alanında etkinleştirilen kazanç yönetimine bağlıdır. İçe aktarma sırasında hatalara neden olacağından, bu alanları **İstihdam Ayrıntısı** varlığında doldurmayın veya güncelleştirmeyin.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint Önizleme bazı ortamlarda çalışmıyor

SharePoint'te depolanan belgelere ait belge önizlemesi çalışmazsa, aşağıdaki yordamı deneyin:

1. Yönetici Kullanıcı hesabının kullanıcı kaydıyla ilişkili bir e-posta olduğunu doğrulayın. Bu bilgileri **Kullanıcı** sayfasında görüntüleyebilirsiniz. E-posta ayarlanmamışsa, OData Excel eklentisi ile e-posta ve sağlayıcı eklemeniz gerekir. Varsayılan olarak, e-posta adresi Excel tasarımında bulunmaz. Excel tasarımını düzenlemeniz, tüm alanları eklemeniz, uygulamanız ve yenilemeniz gerekir. Bu adımları tamamladıktan sonra, yönetici hesabını güncelleştirebilirsiniz.

2. Yönetici hesabının ilişkili bir e-posta hesabı varsa, yönetici kimlik bilgileriyle İnsan Kaynakları için oturum açın.

3. Belge önizlemesini başlatmak için SharePoint ' deki bir eke erişin.

4. Eklere erişimi olan başka bir kullanıcı hesabıyla oturum açın ve önizlemenin beklendiği gibi çalıştığını doğrulayın.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]