---
title: Yazıcı ER hedefi türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için yazıcı hedefini nasıl yapılandırabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 02/14/2022
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
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388300"
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

#### <a name="pdf-printing"></a>PDF yazdırma

10.0.18'den önceki Finance sürümlerinde, **Yazıcı** hedefi, yalnızca, yazdırılabilir PDF biçiminde (**PDF Merger** veya **PDF dosya** biçimi öğeleri) veya Microsoft Office Excel ve Word biçiminde (**Excel dosyası** biçim öğesi) çıktı oluşturmak için kullanılan dosya bileşenleri için yapılandırılabilir. Çıktı PDF biçiminde oluşturulunca yazıcıya gönderilir. Çıktı **Excel dosyası** format biçimi kullanılarak Office biçiminde oluşturulursa otomatik olarak PDF biçimine dönüştürülüp yazıcıya gönderilir.

Ancak, sürüm 10.0.18 itibariyle, **Ortak dosya** biçimi öğesi için **Yazıcı** hedefini konfigüre edebilirsiniz. Bu biçim öğesi çoğunlukla TXT veya XML biçiminde çıktı oluşturmak için kullanılır. Kök biçim öğesi ve **İkili içerikler** biçim öğesi gibi **Ortak dosya** biçimi öğesini içeren bir er biçimini, altındaki tek iç öğe olarak yapılandırabilirsiniz. Bu durumda, **Ortak dosya** biçimi öğesi, **İkili içerik** biçim öğesi için konfigüre ettiğiniz bağlama tarafından belirtilen biçimde çıktıyı üretir. Örneğin, bu bağlamayı, PDF veya Office (Excel veya Word) biçimindeki [Belge yönetimi](../../fin-ops/organization-administration/configure-document-management.md) eki içeriğine sahip öğeyi [dolduracak](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) yapılandırabilirsiniz. Çıktıyı, yapılandırılan **Yazıcı** hedefini kullanarak yazdırabilirsiniz. 

> [!NOTE]
> **Yazıcı** hedefini yapılandırmak için **Ortak\\Dosya** biçim öğesini seçtiğinizde, tasarım süresinde seçili öğenin PDF biçiminde veya PDF biçimine dönüştürülebilecek bir çıktı oluşturacağının garantisi yoktur. Bu nedenle, aşağıdaki uyarı iletisini alırsınız: "Lütfen, seçili biçim bileşeni tarafından oluşturulan çıktının PDF'ye dönüştürülebildiğinden emin olun. Aksi durumda, 'PDF'ye dönüştür' seçeneğinin işaretini kaldırın." Çalışma zamanında yazdırma için PDF veya PDF olmayan çıktı çıkışı sağlandıysa, çalışma zamanı sorunlarını önlemeye yardımcı olacak adımları uygulamanız gerekir. Çıktıyı Office (Excel veya Word) biçiminde almayı bekliyorsanız, **PDF'ye dönüştür** seçeneği işaretlenmiş olmalıdır.
>
> Sürüm 10.0.26 ve sonrasında **PDF'ye dönüştür** seçeneğini kullanmak için konfigüre edilen **Yazıcı** hedefinin **Belge yönlendirme türü** parametresi için **PDF**'yi seçmeniz gerekir.

#### <a name="zpl-printing"></a>ZPL yazdırma

Sürüm 10.0.26 ve sonrasında, **Belge yönlendirme türü** parametresi için **ZPL** öğesini seçerek **Ortak\\Dosya** biçim öğesi için **Yazıcı** hedefini yapılandırabilirsiniz. Bu durumda, çalışma süresinde **PDF'ye dönüştür** seçeneği görmezden gelinir ve TXT veya XML çıktısı doğrudan seçilen yazıcıya [Belge yönlendirme aracısının (DRA)](install-document-routing-agent.md) Zebra Programlama Dili (ZPL) kullanılarak gönderilir. Çeşitli etiketleri yazdırmak için ZPL II etiket düzenini gösteren bir ER biçimi için bu özelliği kullanın.

[![Hedef ayarları iletişim kutusunda Belge yönlendirme türü parametresini ayarlama.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Bu özellik hakkında daha fazla bilgi edinmek için, bkz. [ZPL etiketleri yazdırmak için yeni ER çözümü tasarlama](er-design-zpl-labels.md).

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
