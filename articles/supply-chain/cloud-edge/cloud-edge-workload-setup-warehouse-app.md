---
title: Bulut ve uç ölçek birimleri için Warehouse Management mobil uygulamasını yapılandırma
description: Bu makalede, bir bulut veya uç ölçek birimi tarafından sunulan ambarlar için Warehouse Management mobil uygulamalarınızın nasıl ayarlanacağı açıklanmaktadır.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865252"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için Warehouse Management mobil uygulamasını yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, Warehouse Management mobil uygulamalarınızın bulut veya uç ölçek birimi tarafından sunulan ambarlarda kullanılabilmesi için nasıl ayarlanacağı açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Mobil cihazlarınızı bir bulut veya uç ölçek birimine bağlanacak şekilde ayarlamaya başlamadan önce, kurumsal hub'a bağlanabileceklerini onaylayın. Talimatlar için bkz. [Warehouse Management mobil uygulamasını yükleme ve bağlama](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Warehouse Management mobil uygulamasını bir ölçek birimiyle çalıştırdığınızda ek kurulum

[Ambar ölçek birimi iş yükleri için dağıtım işleminin](cloud-edge-landing-page.md#scale-unit-manager-portal) bir parçası olarak, Warehouse Management mobil uygulama cihazlarınızı bağlamak için gereken verilerin çoğu kurumsal hub'dan ölçek birimine otomatik olarak eşitlenir. Ancak, ölçek birimi dağıtımında, verileri **Azure Active Directory uygulamaları** sayfasına (**Sistem yönetimi \> Kurulum \> Azure Active Directory uygulamaları**) girmelisiniz. Ayrıca, kullanıcı kimliği için varsayılan **Şirket** değerini güncelleştirmeniz veya yeni bir kullanıcı oluşturmanız gerekebilir. Bir ölçek birimi dağıtımında bulunmayan bir şirketle ilişkili kullanıcılar, Warehouse Management mobil uygulaması bu ölçek birimine bağlandığında oturum açamaz.

> [!NOTE]
> **Azure Active Directory uygulamaları** sayfasındaki veriler eşitlenmediği için ambar iş yüklerinizi başka bir ölçek birimine taşımak istiyorsanız bu verileri el ile korumanız gerekir.

Her Warehouse Management mobil uygulamasının bağlantı kurulumunun bir parçası olarak, belirtilen Azure Active Directory kaynak URL'sinin kurumsal hub yerine ölçek birimi için olması gerektiğini unutmayın.
