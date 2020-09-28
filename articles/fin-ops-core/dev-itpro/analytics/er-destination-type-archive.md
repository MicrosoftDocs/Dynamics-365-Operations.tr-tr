---
title: Arşiv ER hedef türü
description: Bu konu, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir arşiv hedefinin nasıl yapılandırılacağı hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745597"
---
# <a name="archive-destination"></a>Arşiv hedefi

[!include [banner](../includes/banner.md)]

Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir arşiv hedefi yapılandırabilirsiniz. Hedef ayarına bağlı olarak, oluşturulan bir belge, ER işleri listesindeki bir kaydın eki olarak depolanır.

Oluşturulan belgeyi Microsoft SharePoint klasörüne veya Microsoft Azure Depolama'ya göndermek için bu seçeneği kullanabilirsiniz. Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet** olarak ayarlayın. Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir. Belge [türlerini](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge türleri**'nde tanımlarsınız. ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.

[![Belge türleri sayfası](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Konum dosyanın kaydedildiği yeri belirler. **Arşiv** hedefi etkinleştirildikten sonra, sonuçlar İş arşivinde kaydedilebilir. Sonuçları **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama arşivlenmiş işler** içerisinde görebilirsiniz.

> [!NOTE]
> **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** \> **Elektronik raporlama parametreleri**'ne giderek İş arşivi için bir belge seçin. Daha fazla bilgi için bkz. [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz. Varsayılan SharePoint sunucusunu tanımlamak için **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge yönetimi parametreleri**'ne gidin. **SharePoint** sekmesinde, SharePoint klasörünü yapılandırın. Sonra, bunu ER çıktısının kaydedileceği klasör olarak seçebilirsiniz. Bu belge türünde **SharePoint** konumunun seçilmesi gerekir.

[![Bir SharePoint klasörü seçmek](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Depolama

Belge türü konumu **Azure depolama** olarak ayarlandığında Azure Depolama'ya bir dosya kaydedebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Belge yönetimini yapılandırma](../../fin-ops/organization-administration/configure-document-management.md)
