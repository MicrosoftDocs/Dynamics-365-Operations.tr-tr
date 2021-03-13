---
title: Yazıcı ER hedefi türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için yazıcı hedefini nasıl yapılandırabileceğiniz açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c6e298f62ec69f349eb713d66313e535c7e01881
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094091"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Yazıcı hedefi

[!include [banner](../includes/banner.md)]

Oluşturulan bir belgeyi doğrudan yazdırma için bir ağ yazıcısına doğrudan gönderebilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, Belge Yönlendirme Aracısı'nı yükleyip yapılandırmanız ve ardından ağ yazıcılarını kaydettirmeniz gerekir. Daha fazla bilgi için bkz. [Ağdan yazdırmayı etkinleştirmek için Belge Yönlendirme Aracısı'nı yükleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Yazıcı hedefini kullanıma açma

**Yazıcı** hedefini Microsoft Dynamics 365 Finance'in geçerli kurulumunda kullanıma açmak için **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri şu sırayla açın:

1. Elektronik Raporlama giden belgelerini Microsoft Office biçimlerinden PDF'e dönüştür
2. Giden belgeler için Elektronik raporlama hedefi olarak Belge Yönlendirme Aracısı

[![Özellik yönetimi'nde ER yazıcı hedefi özelliğini açma](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Uygulanabilirlik

**Yazıcı** hedefi, yalnızca, yazdırılabilir PDF biçiminde (PDF Merger veya PDF dosya biçimi öğeleri) veya Microsoft Office Excel/Word biçiminde (Excel dosyası) çıktı oluşturmak için kullanılan dosya bileşenleri için yapılandırılabilir. Çıktı PDF biçiminde oluşturulunca yazıcıya gönderilir. Çıktı Microsoft Office biçiminde oluşturulursa otomatik olarak PDF biçimine dönüştürülüp yazıcıya gönderilir.

### <a name="limitations"></a>Sınırlamalar

Bu özellik bir önizleme özelliğidir ve 365 Önizleme [Microsoft Dynamics 365 Önizlemeler için Ek Kullanım Koşulları](https://go.microsoft.com/fwlink/?linkid=2105274)'nda açıklanan kullanım koşullarına tabidir.

**Yazıcı** hedefi yalnızca bulut dağıtımları için uygulanır.

### <a name="use-the-printer-destination"></a>Yazıcı hedefini kullanma

1. Oluşturulan belgeyi bir yazıcıya göndermek için **Etkinleştirildi** seçeneğini **Evet** olarak ayarlayın.
2. **Yazıcı adı** alanında, gerekli ağ yazıcısını seçin.
3. Oluşturulan çıktıyı daha sonra yazdırmaya hazır olması için yazdırma arşivinde saklamak için **Yazdırma arşivine kaydedilsin mi?** seçeneğini **Evet** olarak ayarlayın. Arşivlenmiş çıktıya daha sonra erişmek için, **Kuruluş yönetimi** \> **Sorgular ve raporlar** \> **Rapor arşivi**'ne gidin.

[![Yazıcı hedefini kullanma](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **Yazıcı** hedefini yapılandırdığınız zaman, **PDF'e dönüştür** seçeneğinin etkinleştirilmiş olması gerekmez. Seçenek kapalı olsa bile, yazdırma amacıyla PDF dönüştürme işlemi yapılır.

Bir giden belgeyi Excel biçiminde yazdırırken belirli bir [sayfa yönlendirmesini](electronic-reporting-destinations.md#SelectPdfPageOrientation) kullanmak için **PDF'ye Dönüştür** seçeneğini etkinleştirmelisiniz. **PDF 'ye Dönüştür** seçeneğini **Evet** olarak ayarladığınızda, **sayfa yönlendirme** alanı kullanılabilir duruma gelir. **Sayfa yönlendirme** alanında, sayfa yönlendirmesi seçebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
