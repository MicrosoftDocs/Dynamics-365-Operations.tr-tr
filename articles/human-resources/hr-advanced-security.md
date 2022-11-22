---
title: Tüzel kişiliğe göre çalışanlara erişimi kısıtlama
description: Bu makalede, tüzel kişiliğe göre çalışan erişiminin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780401"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Tüzel kişiliğe göre çalışanlara erişimi kısıtlama

Bu makalede, tüzel kişiliğe göre çalışan erişiminin nasıl ayarlanacağı açıklanmaktadır.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Çalışanlar tüzel kişiliklerde istihdam edilir. Burada bazı örnekler verilmiştir:

- Aaron Con, USSI tüzel kişiliğinde istihdam edilmektedir.
- Ahmed Barnett, USMF tüzel kişiliğinde istihdam edilmektedir.
- Alicia Thornber, GLSI ve USMF tüzel kişiliklerinde istihdam edilmektedir.

Kullanıcının şirketteki rolüne bağlı olarak, tüm tüzel kişiliklerdeki çalışanların tümünü görüntülemek için erişim gerekebilir. Alternatif olarak, bir kullanıcının erişimi, yalnızca erişimi olan tüzel kişiliklerdeki çalışanları görebilecek şekilde sınırlı olabilir. Bir kullanıcının hangi çalışanları görüntüleyebileceğini denetlemek için **Human Resources paylaşılan parametreler** sayfasındaki **Çalışan bilgilerine erişimi kısıtla** parametresini seçin.

Örneğin, bir kullanıcının **Çalışan** sayfasına ve yalnızca USMF tüzel kişiliğine erişimi vardır. Bu durumda, Kullanıcı önceki listede bulunan çalışanlar için aşağıdaki bilgileri görüntüleyebilir:

- Çalışan bilgilerine erişimi kısıtlama özelliği etkinleştirilmemişse kullanıcı Aaron, Ahmed ve Alicia'nın bilgilerini görüntüleyebilir.
- Özellik etkinleştirilirse kullanıcı yalnızca Alicia ve Ahmed'in bilgilerini görüntüleyebilir, çünkü bunlar USMF tüzel kişiliğinde istihdam edilmektedir.

Gösterilen bilgiler kullandığınız uygulamaya göre değişir.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources bağımsız

Çalışan bilgilerine erişimi sınırlama özelliği etkinleştirilmişse kısıtlanan kullanıcı çalışan adını içeren bazı listelerde boş bir değer görür.

Örneğin, yalnızca USMF tüzel kişiliğine erişimi olan bir kullanıcı aşağıdaki davranışla karşılaşır:

- Kullanıcının USSI tüzel kişiliğindeki çalışanlara erişimi olmadığından **Etkin pozisyonlar** listesinde **Çalışan** sütunu Aaron'un pozisyonu için boş kalır.
- Kullanıcı, çalışanın adının ayrıntılarına giderse boş bir **Çalışan** sayfası görüntülenir.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources, Finance altyapısında

Çalışan bilgilerine erişimi sınırlama özelliği etkinleştirilmişse kısıtlanan kullanıcı bazı listelerde çalışan adını görür.

Örneğin, yalnızca USMF tüzel kişiliğine erişimi olan bir kullanıcı aşağıdaki davranışla karşılaşır:

- **Etkin pozisyonlar** listesinde **Çalışan** sütunu Aaron'un adını gösterir. Kullanıcı çalışanın adının üzerine geldiğinde, yalnızca ad ve unvan gösterilir.
- Kullanıcı, çalışanın adının ayrıntılarına giderse boş bir **Çalışan** sayfası görüntülenir.

> [!TIP]
> Finance altyapısında Dynamics 365 Human Resources kullanıyorsanız ve sınırlanan kullanıcıların çalışan adları için boş değerler görmesini istiyorsanız **Güvenlik yapılandırması** sayfasındaki kullanıcı rollerine **Çalışanlara erişimi kısıtla** güvenlik ayrıcalığını ekleyebilirsiniz.

Özellik etkinleştirildikten sonra, görünümü sınırlanması gereken her kullanıcıya uygun izinleri ayarlamak için bazı ekstra adımları tamamlamanız gerekir.

1. **Kullanıcılar** sayfasında bir kullanıcı seçin.
2. Kullanıcı için bir rol seçin. **Kuruluşları ata** seçeneği kullanılabilir.
3. **Kuruluşlar ata**'yı seçin.
4. Yeni sayfasında, **Belirli kuruluşlara özel olarak erişim ver** seçeneğini belirleyin ve sonra da kullanıcının erişebileceği kuruluşları seçin.
5. Sistem Kullanıcı rolü de dahil olmak üzere, kullanıcının sahip olduğu her rol için 2 ile 4 arasındaki adımları yineleyin.

> [!NOTE]
> Bir kullanıcının erişimi olan tüzel kişilikler, tüm Kullanıcı rolleri arasında eşleşmelidir.
