---
title: Yazıcı ER hedefi türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için yazıcı hedefini nasıl yapılandırabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b79c93c4920d7f40e88aa7d463961128ea9e83c8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347936"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Yazıcı hedefi

[!include [banner](../includes/banner.md)]

Oluşturulan bir belgeyi doğrudan yazdırma için bir ağ yazıcısına doğrudan gönderebilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, Belge Yönlendirme Aracısı'nı yükleyip yapılandırmanız ve ardından ağ yazıcılarını kaydettirmeniz gerekir. Daha fazla bilgi için bkz. [Ağdan yazdırmayı etkinleştirmek için Belge Yönlendirme Aracısı'nı yükleme](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Yazıcı hedefini kullanıma açma

**Yazıcı** hedefini Microsoft Dynamics 365 Finance'in geçerli kurulumunda kullanıma açmak için **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri şu sırayla açın:

1. Elektronik Raporlama giden belgelerini Microsoft Office biçimlerinden PDF'e dönüştür
2. Giden belgeler için Elektronik raporlama hedefi olarak Belge Yönlendirme Aracısı

[![Özellik yönetimi'nde ER yazıcı hedefi özelliğini açma.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Uygulanabilirlik

**Yazıcı** hedefi, yalnızca, yazdırılabilir PDF biçiminde (PDF Merger veya PDF dosya biçimi öğeleri) veya Microsoft Office Excel/Word biçiminde (Excel dosyası) çıktı oluşturmak için kullanılan dosya bileşenleri için yapılandırılabilir. Çıktı PDF biçiminde oluşturulunca yazıcıya gönderilir. Çıktı Microsoft Office biçiminde oluşturulursa otomatik olarak PDF biçimine dönüştürülüp yazıcıya gönderilir.

### <a name="limitations"></a>Sınırlamalar

**Yazıcı** hedefi yalnızca bulut dağıtımları için uygulanır.

### <a name="use-the-printer-destination"></a>Yazıcı hedefini kullanma

1. Oluşturulan belgeyi bir yazıcıya göndermek için **Etkinleştirildi** seçeneğini **Evet** olarak ayarlayın.
2. **Yazıcı adı** alanında, gerekli ağ yazıcısını seçin.
3. Oluşturulan çıktıyı daha sonra yazdırmaya hazır olması için yazdırma arşivinde saklamak için **Yazdırma arşivine kaydedilsin mi?** seçeneğini **Evet** olarak ayarlayın. Arşivlenmiş çıktıya daha sonra erişmek için, **Kuruluş yönetimi** \> **Sorgular ve raporlar** \> **Rapor arşivi**'ne gidin.

[![Yazıcı hedefini kullanma.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **Yazıcı** hedefini yapılandırdığınız zaman, **PDF'e dönüştür** seçeneğinin etkinleştirilmiş olması gerekmez. Seçenek kapalı olsa bile, yazdırma amacıyla PDF dönüştürme işlemi yapılır.

Bir giden belgeyi Excel biçiminde yazdırırken belirli bir [sayfa yönlendirmesini](electronic-reporting-destinations.md#SelectPdfPageOrientation) kullanmak için **PDF'ye Dönüştür** seçeneğini etkinleştirmelisiniz. **PDF 'ye Dönüştür** seçeneğini **Evet** olarak ayarladığınızda, **sayfa yönlendirme** alanı kullanılabilir duruma gelir. **Sayfa yönlendirme** alanında, sayfa yönlendirmesi seçebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]