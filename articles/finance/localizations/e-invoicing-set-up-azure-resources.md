---
title: Elektronik faturalama için Azure kaynaklarını ayarlama
description: Bu konu, Elektronik faturalama için Microsoft Azure kaynakları kurulumu ve konfigüre etme işlemine genel bakış sağlar.
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
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371776"
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
