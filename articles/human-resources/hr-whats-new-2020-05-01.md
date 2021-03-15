---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (1 Mayız 2020)
description: Bu makalede, 1 Mayıs 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 05/01/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e41762e4283d5a4b0c9dd8359c5fb2bdabfc26
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127885"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (1 Mayız 2020)

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3196 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Veri Yönetim Çerçevesinde (DMF) kullanılabilir olan Yeni Performans Yönetimi varlıkları

Aşağıdaki varlıklar artık kullanılabilir. Varlıklar listesinde bu varlıkları listelenmiş olarak göremezseniz, **Çerçeve Parametreleri > VArlık ayarları > Varlık listesini yenile**'deki **Varlıkları yenile** seçeneğini kullanın.

- **Tartışma Yetkinliği**
- **Tartışma Hedefleri**
- **Tartışma Ölçümü**
- **Tartışma Konusu**
- **Performans Günlüğü**
- **Ölçüm**
- **Hedef Ölçümü**

Ek olarak, **Tartışma** varlığına **Toplam puan** ve **Ortalama puan** eklendi.

## <a name="increase-length-of-leave-request-comments-275641"></a>İzin isteği açıklamalarının uzunluğunu artırma (275641)

İzin isteklerindeki açıklamalar için artık 100'den fazla karaktere izin veriliyor.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>İncelemelerdeki son açıklamalar, yönetici veya personel farklı bir şirkette oturum açtığında görünmüyor (431688)

Artık tüm açıklamalar incelemeler görüntülendiğinde görünüyor.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Kullanıcı tanımlı bağlantılar yeni Çalışan formunda desteklenmiyor (390374)

Kullanıcı tanımlı bağlantılar artık kolaylaştırılan **Çalışan** formunda etkin durumda.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity OData API kilitlenmesine neden oluyor (439476)

Bu değişiklik API kilitlenmesini düzeltir. Bu hataya yinelenen bir ad neden oluyordu.

## <a name="in-preview"></a>Ön izlemede

## <a name="leave-suspension"></a>İzni askıya alma

Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Tahakkukun askıya alınmış olduğunu belirtmek için kullanıcı deneyimini güncelleştirme (429550)

Kullanıcı deneyimi şimdi tahakkukun bir plan için askıya alınmış olduğunu gösteriyor.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Belirtilen izin türleri için izin tahakkunu askıya alma (272447)

Bu sürümde İK, ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilir. Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez. Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir (429549)

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Tahakkuk askıya almalara neden kodu ekleme (429547)

Neden kodları tahakkuk askıya almaya eklenmiştir.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>İnsan Kaynakları parametrelerinden izin ve devamsızlık parametrelerine geçişi başlat

Bu sürüm İnsan Kaynakları parametrelerini İzin ve devamsızlık parametreleriyle birleştirmeye başlar.

## <a name="carry-forward-rules"></a>Devretme kuralları

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Bilinen sorunlar

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint Önizleme bazı ortamlarda çalışmıyor

SharePoint'te depolanan belgelere ait belge önizlemesi çalışmazsa, aşağıdaki yordamı deneyin:

1. Yönetici Kullanıcı hesabının kullanıcı kaydıyla ilişkili bir e-posta olduğunu doğrulayın. Bu bilgileri **Kullanıcı** sayfasında görüntüleyebilirsiniz. E-posta ayarlanmamışsa, OData Excel eklentisi ile e-posta ve sağlayıcı eklemeniz gerekir. Varsayılan olarak, e-posta adresi Excel tasarımında bulunmaz. Excel tasarımını düzenlemeniz, tüm alanları eklemeniz, uygulamanız ve yenilemeniz gerekir. Bu adımları tamamladıktan sonra, yönetici hesabını güncelleştirebilirsiniz.

2. Yönetici hesabının ilişkili bir e-posta hesabı varsa, yönetici kimlik bilgileriyle İnsan Kaynakları için oturum açın.

3. Belge önizlemesini başlatmak için SharePoint ' deki bir eke erişin.

4. Eklere erişimi olan başka bir kullanıcı hesabıyla oturum açın ve önizlemenin beklendiği gibi çalıştığını doğrulayın.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]