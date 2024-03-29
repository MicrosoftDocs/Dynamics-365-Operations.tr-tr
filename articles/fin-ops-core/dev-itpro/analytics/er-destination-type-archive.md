---
title: Arşiv ER hedef türü
description: Bu makalede, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için arşiv hedefinin nasıl yapılandırılacağı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: d907bf391c0629d62da489cea90a05eabaf69ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285470"
---
# <a name="archive-er-destination-type"></a>Arşiv ER hedef türü

[!include [banner](../includes/banner.md)]

Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her **Klasör** veya **Dosya** bileşeni için bir arşiv hedefi yapılandırabilirsiniz. Hedef ayarına bağlı olarak, oluşturulan bir belge, ER işleri listesindeki bir kaydın eki olarak depolanır. Sonuçları görüntülemek için **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri** öğesine gidin.

Oluşturulan belgeyi Microsoft SharePoint klasörüne veya Microsoft Azure Depolama'ya göndermek için bu seçeneği kullanabilirsiniz. Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet** olarak ayarlayın. Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir. Belge [türlerini](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge türleri**'nde tanımlarsınız. ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.

[![Belge türleri sayfası.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Konum dosyanın kaydedildiği yeri belirler. **Arşiv** hedefi etkinleştirildikten sonra, sonuçlar İş arşivinde kaydedilebilir. Sonuçları **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama arşivlenmiş işler** içerisinde görebilirsiniz.

> [!NOTE]
> **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** \> **Elektronik raporlama parametreleri**'ne giderek İş arşivi için bir belge seçin. Daha fazla bilgi için [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) konusuna bakın.

## <a name="sharepoint"></a>SharePoint

Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz. Varsayılan SharePoint sunucusunu tanımlamak için **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge yönetimi parametreleri**'ne gidin. **SharePoint** sekmesinde, SharePoint klasörünü yapılandırın. Sonra, bunu ER çıktısının kaydedileceği klasör olarak seçebilirsiniz. Bu belge türünde **SharePoint** konumunun seçilmesi gerekir.

[![Bir SharePoint klasörü seçme.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Depolama

Belge türü konumu **Azure depolama** olarak ayarlandığında Azure Depolama'ya bir dosya kaydedebilirsiniz.

> [!NOTE] 
> İşlenmesi gereken belgeler için 7 gün saklama politikası uygulayan Veri yönetimi çerçevesinin aksine, ER çerçevesi dosyaları kalıcı olarak Azure Blob depolama alanında depolar. Daha fazla bilgi için bkz. [İleti durumu alma API'si](../data-entities/recurring-integrations.md#api-for-getting-message-status) ve [Durum denetimi API'si](../data-entities/data-management-api.md#status-check-api). ER ile ilgili dosyalar, gerekli olduğu sürece, Azure Blob depolamada, uygulama tablosu kayıtlarının ekleri olarak depolanır. Azure Blob depolama alanından bu dosyanın eklendiği uygulama tablosu kaydıyla birlikte tek bir dosya silinir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Belge yönetimini yapılandırma](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
