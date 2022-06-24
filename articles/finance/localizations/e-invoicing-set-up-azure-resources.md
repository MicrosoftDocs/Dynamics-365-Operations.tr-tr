---
title: Elektronik faturalama için Azure kaynaklarını ayarlama
description: Bu makalede, Elektronik faturalama için Microsoft Azure kaynaklarını ayarlama işlemine genel bakış sağlanmaktadır.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907743"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Elektronik faturalama için Azure kaynaklarını ayarlama

[!include [banner](../includes/banner.md)]

Elektronik faturalama için Microsoft Azure kaynak ayarlama süreci üç adımdan oluşur. İlk iki adım, "Azure portalında bir Azure Key Vault oluşturma" ve "Azure portalında bir Azure depolama hesabı oluşturma", zorunludur. Üçüncü adım, "SharePoint bağlantısı yapılandırma", isteğe bağlıdır.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Azure portalda Azure Key Vault oluşturma

Azure aboneliğinizde anahtar kasası oluşturun. Elektronik faturalama için ayrı bir anahtar kasa oluşturmanızı ve gizli dizileri diğer uygulamalarla birleştirmemenizi öneririz. Elektronik belgelerdeki senaryolarınız için gerektiği kadar gizli dizi ve sertifika oluşturun. Sonraki adımda oluşturacağınız Azure depolama hesabının paylaşılan erişim imzası (SAS) belirtecini depolamak için en az bir gizli kod dizesi oluşturmalısınız.

Bu adımı tamamlama hakkında bilgi için bkz. [Azure portalında Azure Key Vault oluşturma](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure portalda Azure depolama hesabı oluşturma

Elektronik faturalama servisi tarafından oluşturulan veya servise giren elektronik belge ve dosyaların tümü size aittir. Bu belge ve dosyalar, Azure aboneliğinizde oluşturduğunuz bir Azure depolama hesabında depolanır. Hizmet, Key Vault gizli dizisinden alınan SAS belirtecini kullanarak depolama hesabınıza erişir.

Bu adımı tamamlama hakkında bilgi için bkz. [Azure portalında Azure depolama hesabı oluşturma](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePoint bağlantısını yapılandırma

Bazı senaryolarda, elektronik dosyaları SharePoint'e kaydetmeniz ve bunları SharePoint'ten almanız gerekebilir. Elektronik faturalama hizmetinin SharePoint klasörlerinize erişebilmesini sağlamak için SharePoint'e erişimi konfigüre edin.

Bu adımı tamamlama hakkında bilgi için bkz. [SharePoint bağlantısı yapılandırma](e-invoicing-create-sharepoint-connection.md).
