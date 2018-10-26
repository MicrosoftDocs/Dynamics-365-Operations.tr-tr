---
title: "Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (Ekim 1, 2018)"
description: "Bu konuda, Microsoft Dynamics 365 for Talent Core HR'deki yeni veya değişen özellikler açıklanmaktadır."
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.contentlocale: tr-tr
ms.lasthandoff: 10/01/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (Ekim 1, 2018)

[!include [banner](includes/banner.md)]

**Derleme 8.1.1035.0**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="turn-off-electronic-payment-validation"></a>Elektronik ödeme doğrulamasını kapatma

Elektronik Ödeme bilgileri doğrulaması, **Çalışan Self-Servisi** çalışma alanı (ESS) veya doğrudan çalışan formunda doğrudan havale için tahsilat ayarladıysanız ortaya çıkar. Bu seçenek, tutarlar ve kalan değerler için doğrulama denetimleri gerektirmiyorsa bu doğrulamayı kaldırma esnekliği sunar. Bu özellik, farklı gereksinimleri olan harici bir ödeme sistemiyle entegrasyon yapıyorsanız faydalıdır.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Yönetici Self-Servis - Ekip performans hedefleri kutucuğu üzerinden ekip üyelerine hedefler ekleme

Bu sürümden önce, yöneticiler çalışanlarına bireysel olarak performans hedeflerini doğrudan atayabilmektelerdi. Bu güncelleştirme ile yöneticiler, **Ekip performans hedefleri** kutucuğuna erişebilir ve doğrudan altlarından herhangi birine yeni hedefler ekleyebilirler.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Yönetici Self-Servis - Ekip performans gözden geçirmeleri kutucuğu üzerinden ekip üyelerine gözden geçirmeler ekleme

Bu sürümden önce, yöneticiler çalışanlarına bireysel olarak performans gözden geçirmeleri doğrudan atayabilmektelerdi. Bu güncelleştirme ile yöneticiler, **Ekip performans gözden geçirmeleri** kutucuğuna erişebilir ve doğrudan altlarından herhangi birine yeni gözden geçirmeler ekleyebilirler.

## <a name="configure-proration-options-by-leave-plan"></a>Bırakma planına göre dağıtma yapılandırma

Kuruluşlar, çalışanların şirkete ne zaman katıldığı ve çıktığına dayalı olarak farklı izinler verirler. Bazı kuruluşlarda çalışanlara tam haklarını başlangıçta verirken, diğerleri bölüştürme yapar. Bu dağıtımda, kuruluşa katılan ve ayrılanlar için ödüllerin nasıl dağıtılacağını seçme olanağı sunulmaktadır. Seçeneklere şunlar dahildir: Bölünen, tam tahakkuk ve tahakuk yok.

## <a name="other-changes"></a>Diğer değişimler

-   Çalışan varlığı güncelleştirildi - **Kişisel** kutucuk artık Excel eklentisi/veri yönetimi kullanılarak güncelleştirilebilir.

-   Ödeme bilgisi için personel self servisindeki **Sil** ve **Devre dışı bırak** düğmelerinin kaldırılmasına izin vermek için güvenlik değişikliği.

## <a name="known-issue"></a>Bilinen sorun

-   **Sorun:** Bir çalışana yeni bir eklenti eklerken, **Yeni** ve **Düzenle** düğmeleri gri haldedir. **Geçici çözüm:** Eklenti sayfasını açmadan önce, **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, **Eklentiler** düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)

