---
title: Cinsiyet temel sabit listesi genişletilebilirliği
description: Bu makalede Cinsiyet temel sabit listesinin genişletilebilirliğine genel bakış sunulmaktadır.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749324"
---
# <a name="gender-base-enum-extensibility"></a>Cinsiyet temel sabit listesi genişletilebilirliği

**Cinsiyet** sabit listesi artık genişletilebilir. Bu makalede **Cinsiyet** sabit listesini genişletmek için kod tabanında yapmanız gereken değişiklikler açıklanmaktadır.

## <a name="gender-vs-hcmpersongender"></a>Cinsiyet ile HcmPersonGender karşılaştırması

Cinsiyet değerleri için iki sabit liste vardır:

- **Cinsiyet** (Uygulama Platformu)
- **HcmPersonGender** (PersonnelManagement)

**Cinsiyet** sabit listesi Microsoft Dynamics 365 Finance'te kullanılırken, **HcmPersonGender** insan sermayesi yönetimi (HCM) işlevine özgüdür. HCM işlevlerini kullanıyorsanız ve **Cinsiyet** sabit listesinde değişiklik yaparsanız, aynı değişiklikleri **HcmPersonGender** için de yapmanız gerekir. Örneğin, **Cinsiyet** sabit listesine **Transseksüel** eklediğinizde, **HcmPersonGender** sabit listesine de **Transseksüel** öğesini ekleyin.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (Sınıf)

İki temel sabit liste arasında çeviriye izin vermek için yeni bir **HcmPersonGenderTranformUtil** sınıfı oluşturuldu. Bu sınıfta, **convertGenderToHcmPersonGender** ve **convertHcmPersonGenderToGender** olmak üzere iki yöntem bulunmaktadır. **Komut Zinciri** sınıfını ya da **olay işleyicilerini** kullanarak bir uzantı oluşturup iki yöntemi de sabit listelerine eklenen yeni değerleri eşlemek üzere genişletmeniz gerekir.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (Sınıf)

**PayrollStateWageTaxPrepDP**, **Bordro Durumu Ücret Vergisi Hazırlığı** SQL Server Reporting Services (SSRS) raporunun veri sağlayıcı sınıfıdır. Amerika Birleşik Devletleri'nde üç değer kullanılmaktadır: **Erkek**, **Kadın** ve **Belirtilmemiş**. **populatePayrollStateWageTaxPrepTmp** yönteminde, **HcmPersonGender** sabit listesi değerini **IsMale**, **IsFemale** veya **IsUnspecifiedGender** alanlarından birine eşlemek için kullanılan bir geçiş ifadesi bulunmaktadır. Geçiş ifadesinin varsayılan değeri **IsUnspecifiedGender**'dır. **HcmPersonGender** sabit listesine farklı şekilde eşlenecek değerler eklerseniz, değeri gerektiği gibi değiştirmek için **populatePayrollStateWageTaxPrepTmp** yöntemine **Komut Zinciri** sınıfı kullanarak bir uzantı oluşturmanız gerekir.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (Sınıf)

**smmOutlookSync_Contact** tümleştirme sınıfı **Outlook** ve **İlgili kişiler** arasında değerleri bağlar. **Outlook**, **Erkek**, **Kadın** ve **Belirtilmemiş** olmak üzere üç değeri destekler. Bu sınıfta **Cinsiyetler** ile **OutlookGenders** eşlemenize yardımcı olacak iki yöntem vardır. Varsayılan yöntem **NonSpecific/UnSpecified** olarak belirlenmiştir. **Cinsiyet** sabit listesi için ek değer oluşturursanız, iki yöntem için de **Komut Zinciri** sınıfını kullanarak bir uzantı oluşturup gerektiği şekilde eşlemelisiniz.
