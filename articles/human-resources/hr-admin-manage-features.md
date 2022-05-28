---
title: Human Resources özellikleri yönetme
description: Bu konu Özellik Yönetimi özelliğini ve nasıl kullanabileceğinizi açıklar.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 914752e71871ce05255fbb52ad6a0ee8f0226a4c
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687317"
---
# <a name="manage-features-in-human-resources"></a>Human Resources özellikleri yönetme


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources için sürekli olarak kullanıma sunduğumuz yeni yeteneklerin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz. Neredeyse genel kullanıma hazır ve kapsamlı bir sınamadan geçirilmiş önizleme özelliklerini sunacağız. Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.

İnsan Kaynakları'ndaki yeni özellikler hakkında daha fazla bilgi için bkz. [İnsan Kaynakları'ndaki yenilikler](hr-admin-whats-new.md) ve [Dynamics 365 ve Power Platform Sürüm Planı](/dynamics365/release-plans/?panel=products1#pivot=products).

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.

Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

## <a name="enable-or-disable-preview-features"></a>Önizleme özelliklerini etkinleştirme veya devre dışı bırakma

Önizleme özelliklerine erişmek için, önce ortamınızda etkinleştirmeniz gerekir. Önizleme özelliklerini devre dışı bırakma veya etkinleştirme ortama özgüdür.

> [!IMPORTANT]
> Önizleme özellikleri yalnızca **korumalı alan** ortamlarında etkinleştirilecek. Önizleme özelliğini açtığınız zaman, kuruluşunuzda bulunan bu ortamdaki tüm kullanıcılar için etkinleştirmiş olursunuz. Önizleme özelliğini kapattığınız zaman devre dışı bırakmış ve kullanıcılarınızın erişimine kapatmış olursunuz. Önizleme özellikleri İnsan Kaynakları'nda sınırlı şekilde desteklenmektedir. Bu özellikler daha az gizlilik ve güvenlik önemi kullanabilir ve İnsan Kaynakları hizmet düzeyi sözleşmesine (SLA) dahil değildirler. Kişisel verileri (diğer bir deyişle, sizi tanımlamaya yardımcı olabilecek tüm bilgileri) işlemek ya da yasa veya düzenlemelerle uyumluluk gereksinimlerine tabi olan diğer verileri işlemek için önizleme özelliklerini kullanmamanız gerekir.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Özellik yönetimi** kutucuğunu seçin.

3. Bir önizleme özelliğini etkinleştirmek için, özelliği listeden seçin ve ardından **Etkinleştir**'i seçin. Bir önizleme özelliğini devre dışı bırakmak için, özelliği listeden seçin ve ardından **Devre dışı bırak**'ı seçin.

## <a name="enable-or-disable-benefits-management"></a>Kazanç yönetimini etkinleştirme veya devre dışı bırakma

Kazanç yönetimini etkinleştirmek için [Önizleme özelliklerini etkinleştirme veya devre dışı bırakma](hr-admin-manage-features.md?enable-or-disable-preview-features)'daki aynı prosedürü kullanın.

> [!IMPORTANT]
> Etkinleştirdikten sonra **Üretim** ortamında Kazanç yönetimini devre dışı bırakamazsınız. Ancak, Kazanç yönetimini **Korumalı alan** ortamında devre dışı bırakabilirsiniz.

Kazanç yönetimi yapılandırması ve kullanımı hakkında daha fazla bilgi için bkz. [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md).

Kazanç yönetimi, **Kazançlar** çalışma alanındaki işlevlerin yerini alıyor. Kazanç yönetimi önizleme özelliğini etkinleştirdiğiniz zaman, artık **Kazançlar** çalışma alanında şu formlara erişemezsiniz:

- **Kazançlar**
- **Kazanç öğeleri**
- **Katkı hesaplama oranları**
- **Kazanç kayıt sonuçları**
- **Kazanç geçerlilik süresini bitirme ve uzatma sonuçları**
- **Kazanç uygunluğu ilke kuralı türleri**
- **Kazanca uygunluk ilkeleri**
- **Uygunluk olayları**

Bu sayfalardaki bilgileri salt okunur modda görüntüleyebilirsiniz. Bilgileri düzenlemek isterseniz, önce Kazanç yönetimini devre dışı bırakmanız gerekir (yalnızca **Korumalı alan** ortamlarına uygulanır).

## <a name="enable-or-disable-leave-and-absence"></a>İzin ve devamsızlığı etkinleştirme veya devre dışı bırakma

İzin ve devamsızlığı etkinleştirmek için [Önizleme özelliklerini etkinleştirme veya devre dışı bırakma](hr-admin-manage-features.md?enable-or-disable-preview-features)'daki aynı prosedürü kullanın.

> [!IMPORTANT]
> İzin ve devamsızlıkta etkinleştirdikten sonra **Birden fazla izin türü** özelliğini devre dışı bırakamazsınız. Bu durum hem **Korumalı alan** hem de **Üretim** ortamları için geçerlidir.

İzin ve devamsızlık'taki önizleme özellikleri hakkında daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Geri bildirim gönderin

Bu önizleme özellikleriyle ilgili deneyiminizden haberdar olmak istiyoruz. Bu özellikleri veya diğer yeni özellikleri kullandıkça aşağıdaki sitelerden bize düzenli olarak geribildirim göndermenizi rica ediyoruz:

- [Topluluk](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Bu, kullanıcıların olayları tartışabileceği, sorular sorabileceği ve topluluktan yardım alabileceği yararlı bir kaynaktır.
- Üründe görmek istediğiniz özellikleri ve mevcut özellikler için yapmamız gerektiğini düşündüğünüz herhangi bir değişikliği bize bildirin. [Human Resources fikirleri](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)'nde ürünlerle ilgili fikirler önerin.
    
Lütfen kişisel verilerinizi (sizi tanımlamaya yardımcı olabilecek bilgileri) geri bildiriminize veya ürün incelemesi gönderimlerinize eklemeyin. Toplanan bilgiler daha ayrıntılı incelenebilir ve yürürlükteki gizlilik yasaları kapsamında talepleri yanıtlamak için kullanılamaz. Bu programlar altında ayrı olarak toplanan kişisel veriler [Microsoft Gizlilik Bildirimi](https://privacy.microsoft.com/privacystatement)'ne tabidir.

## <a name="see-also"></a>Ayrıca bkz.

- [İnsan Kaynakları'ndaki yenilikler](hr-admin-whats-new.md)
- [Dynamics 365 ve Power Platform Sürüm Planı](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
