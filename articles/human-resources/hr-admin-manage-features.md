---
title: Özellikleri yönetme
description: Dynamics 365 Human Resources'ta yeni özelliklerin nasıl açıldığı veya kapatıldığını öğrenin.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9176e9519c3bf65ef7a4f1b5ae43dbeb411750f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420977"
---
# <a name="manage-features"></a>Özellikleri yönetme

Microsoft Dynamics 365 Human Resources için sürekli olarak kullanıma sunduğumuz yeni yeteneklerin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz. Neredeyse genel kullanıma hazır ve kapsamlı bir sınamadan geçirilmiş önizleme özelliklerini sunacağız. Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.

İnsan Kaynakları'ndaki yeni özellikler hakkında daha fazla bilgi için bkz. [İnsan Kaynakları'ndaki yenilikler](hr-admin-whats-new.md) ve [Dynamics 365 ve Power Platform Sürüm Planı](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

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

Bu formlardaki bilgileri salt okunur modda görüntüleyebilirsiniz. Bilgileri düzenlemek isterseniz, önce Kazanç yönetimini devre dışı bırakmanız gerekir (yalnızca **Korumalı alan** ortamlarına uygulanır).

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
- [Dynamics 365 ve Power Platform Sürüm Planı](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)