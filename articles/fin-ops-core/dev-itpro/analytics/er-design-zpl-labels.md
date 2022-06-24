---
title: ZPL etiketleri yazdırmak için yeni bir ER çözümü tasarlama
description: Bu makalede, Zebra Programlama Dili (ZPL) etiketleri yazdırmak için yeni bir Elektronik raporlama (ER) çözümünün nasıl tasarlanacağı açıklanmaktadır.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f861fe63c6d7d00d0a9f84d33c0d1b1b23735b61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845729"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>ZPL etiketleri yazdırmak için yeni bir ER çözümü tasarlama

[!include [banner](../includes/banner.md)]


Bu makalede Sistem Yöneticisi, Elektronik Raporlama Geliştiricisi veya Elektronik Raporlama İşlevsel Danışmanı rolüne sahip bir kullanıcının [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesinin parametrelerini nasıl yapılandırabileceği, Ambar yönetimi sistemi verilerine erişmek için yeni bir ER çözümünün gerekli ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) nasıl tasarlayabileceği ve nasıl Zebra Programlama Dili (ZPL) II biçiminde özel ambar konumu etiketleri oluşturabileceği açıklanmaktadır. Bu adımlar **USRT** şirketinde gerçekleştirilebilir.

## <a name="business-scenario"></a>İş senaryosu

Microsoft Dynamics 365 Finance'te ambar yönetimini uygulayan bir şirketi temsil ediyorsunuz. Her ambar konumu, bir barkod içeren, kendi kendine bağlanan bir etiketle etiketlenmelidir. Ambar çalışanları, barkodları taramak için elle tutulan barkod okuyucularını kullanır.

Servise alma öncesi etkinlikler kapsamında tüm ambar yerleşimleri etiketlendi. Ancak, varolan etiketlerin zarar görmesi veya ambarda rafa kaldırma yeniden yapılandırılması durumunda ambar konumu etiketlerini de yazdırmanız gerekir. En son yayınlanan ER işlevlerini kullanarak, bir ambar gözetmeninin etiketleri ısı etiketi yazıcısına doğrudan yazdırmasını sağlayan yeni bir ER çözümü konfigüre edebilirsiniz.

## <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. Yeni bir ER çözümü tasarlamak için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

## <a name="design-a-domain-specific-data-model"></a>Etki alanına özel veri modeli tasarlama

Ambar yönetimi etki alanı için [veri modeli](er-overview-components.md#data-model-component) bileşeni içeren yeni bir ER yapılandırması oluşturun. Bu veri modeli daha sonra ambar konumu etiketleri raporu oluşturmak üzere bir ER biçimi tasarlarken veri kaynağı olarak kullanılacaktır.

### <a name="import-a-data-model-configuration"></a>Veri modeli yapılandırmasını içe aktarma

Gerekli veri modelini Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin. Alternatif olarak, sonraki bölümde açıklandığı gibi kendi veri modelinizi de oluşturabilirsiniz.

1. [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Warehouse model.version.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER veri modeli yapılandırması.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Bir veri modeli yapılandırması oluşturun

Microsoft tarafından sağlanan veri modeli dosyasını içe aktarmak yerine, sıfırdan bir veri modeli oluşturabilirsiniz. Bu görevin nasıl tamamlandığını gösteren bir örnek için, bkz. [Yeni bir veri modeli yapılandırması oluşturma](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Veri modelini gözden geçirme

Konfigüre edilen veri modelinin düzenlenebilir sürümünü **Veri modeli tasarımcısı** sayfasında görüntüleyebilirsiniz.

![Veri modeli tasarımcısı sayfasındaki ER veri modelinin yapısı.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Yapılandırılan veri modeli için bir model eşlemesi tasarlama

Elektronik Raporlama Geliştirici rolünde bir kullanıcı olarak, Ambar veri modeli için bir [model eşleme](er-overview-components.md#model-mapping-component) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu bileşen Dynamics 365 Finance için yapılandırılmış veri modelini uygular ve bu uygulamaya özgüdür. Yapılandırılan veri modelini çalışma zamanında uygulama verileriyle doldurmak için kullanılması gereken uygulama nesnelerini belirtecek şekilde yapılandırmanız gerekir. Bu görevi tamamlamak için, Finance'te Ambar yönetimi iş etki alanının veri yapısı uygulama ayrıntılarını bilmeniz gerekir.

### <a name="import-a-model-mapping-configuration"></a>Model eşlemesi yapılandırmasını içe aktarma

Gerekli model eşlemeyi Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin. Alternatif olarak, sonraki bölümde açıklandığı gibi kendi model eşlemenizi de oluşturabilirsiniz.

1. [Warehouse model mapping.version.1.1xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Warehouse model mapping.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER model eşleme yapılandırması.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Model eşleme yapılandırması oluşturma

Microsoft tarafından sağlanan model eşlemesi dosyasını içe aktarmak yerine, sıfırdan bir model eşlemesi oluşturabilirsiniz. Bu görevin nasıl tamamlandığını gösteren bir örnek için, bkz. [Yeni bir model eşlemesi yapılandırması oluşturma](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Model eşlemeyi gözden geçirme

Konfigüre edilen model eşlemesinin düzenlenebilir sürümünü **Model eşlemesi tasarımcısı** sayfasında görüntüleyebilirsiniz.

![Model eşlemesi tasarımcısı sayfasındaki ER model eşlemesi yapısı.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Bir biçim tasarlama

Elektronik Raporlama İşlev Danışmanı rolündeki bir kullanıcı olarak, bir [biçim](er-overview-components.md#format-component) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu bileşeni yapılandırmak için, ambar konumu etiketinin düzenini belirtmek üzere ZPL II kodunu kullanırsınız.

### <a name="import-a-format-configuration"></a>Bir biçim yapılandırmasını içe aktarma

Gerekli biçimi Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin. Alternatif olarak, sonraki bölümde açıklandığı gibi kendi biçiminizi de oluşturabilirsiniz.

1. [Warehouse location labels.version.1.1xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Warehouse location labels.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER biçim yapılandırması.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Biçim yapılandırması oluşturma

Microsoft tarafından sağlanan biçim dosyasını içe aktarmak yerine, sıfırdan bir biçim oluşturabilirsiniz. Bu görevin nasıl tamamlandığını gösteren bir örnek için, bkz. [Yeni bir biçim yapılandırması oluşturma](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Biçimi gözden geçirme

Konfigüre edilen biçimin düzenlenebilir sürümünü **Biçim tasarımcısı** sayfasında görüntüleyebilirsiniz.

![Biçim tasarımcısı sayfasındaki ER biçiminin yapısı.](./media/er-design-zpl-labels-format.png)

Bu biçimin `model.Location.Label` veri kaynağı, aşağıdaki bilgileri içeren etiketler oluşturmak üzere yapılandırılmıştır:

- Metin olarak ambar başlığı
- Barkod olarak ambar başlığı
- Konum başlığı
- Kontrol basamakları

Veri kaynağının **Formül tasarımcısı** sayfasında, etiket oluşturmak için kullanılan ER formülü, bilgileri istenen düzende birleştiren bir `CONCATENATE` işlevi içerir.

![Formül tasarımcı sayfasındaki veri kaynağının formülü.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Etiket yerleşimi, yerleşim başlığı ve çek basamakları etiketin ortasına hizalanacak şekilde tasarlanmıştır. Ancak ZPL II, barkodların orta hizalamasını desteklemez. Bu nedenle, `model.Location.Warehouse.Alignment` veri kaynağının formülü, barkodu etiketin ortasına hizalamak için kullanılır. Bu formül, ambar başlığındaki karakter sayısına göre barkod sol uzaklığını hesaplar.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Oluşturulan etiketlerin önizlemesini görüntülemek için ortamınızı hazırlayın

Aşağıdaki örnek, ekranda oluşturulan etiketlerin önizlemesini göstermek için, ZPL etiketleri için bir yazıcı öykünücüsü uygulaması kullanır. Bu seçeneği etkinleştirmek için bu adımları izleyin.

1. **Ambar konumu etiketi** ER biçimi için [Yazıcı](er-destination-type-print.md) ER hedefini ekleyin ve bunu Finance'ten [Belge yönlendirme aracısına (DRA)](install-document-routing-agent.md) oluşturulan etiketleri gönderecek şekilde konfigüre edin.
2. Finance'ten oluşturulan etiketleri geçerli iş istasyonundan erişilebilen bir yerel yazıcıya yönlendirmek için DRA'yı yükleyin ve konfigüre edin.
3. Geçerli iş istasyonu için yerel bir yazıcı ekleyin ve bu yazıcıyı, oluşturulan etiketleri DRA'dan bir yazıcı öykünücüsü uygulamasına geçirecek şekilde yapılandırın.
4. Chrome web tarayıcısının bir eklentisi olarak bir yazıcı öykünücüsü uygulaması yükleyin ve bunu, oluşturulan etiketleri yerel yazıcıdan, oluşturulan etiketleri işleyerek önizleme için yazıcı öykünücüsüne döndürecek bir web hizmetine geçirecek şekilde yapılandırın.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER raporu</p>
<p>Yazıcı hedefi</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Belge yönlendirme aracısı</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Yerel yazıcı</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Yazıcı öykünücüsü</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Web hizmetini işleme</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Yazıcı öykünücü uygulamasını yükleme ve konfigüre etme

Chrome web tarayıcınıza ZPL işleme altyapısı için bir yazıcı öykünücüsü uygulaması ekleyin. Bu örnek, [Labelary ZPL web hizmeti](http://labelary.com/service.html) temelli [Zpl Yazıcısı](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) öykünücüsünü kullanır. Yazıcı öykünücüsü, oluşturulan etiketleri yerel bir yazıcıdan web servisine dönüştürür ve daha sonra etiketleri önizleme için PDF veya PNG dosyaları olarak geri döndürecektir.

1. Chrome web mağazasında, kullanmak istediğiniz yazıcı öykünücüsü uygulamasını bulun ve seçin. Daha sonra bunu Chrome web tarayıcınıza eklemek için, **Chrome'a ekle**'yi seçin.

    ![Yazıcı öykünücü uygulamasını, Chrome web mağazasından Chrome web tarayıcısına ekleme.](./media/er-design-zpl-labels-add-app.png)

2. Chrome web tarayıcısından yazıcı öykünücüsü uygulamasını çalıştırmak için **Uygulamayı başlat**'ı seçin.

    ![Chrome web tarayıcısından yazıcı öykünücüsü uygulamasını çalıştırma.](./media/er-design-zpl-labels-run-app.png)

3. Çalıştırılan uygulamayı yapılandırma:

    1. Uygulamayı kapatın.
    2. Yazıcı ayarlarında, ana bilgisayarı **127.0.0.1** olarak ayarlayın.
    3. Bağlantı noktasını **9100** olarak ayarlayın.

        ![Yazıcı öykünücüsü uygulamasını yapılandırma.](./media/er-design-zpl-labels-configure-app.png)

    4. Uygulamayı tekrar açın. Belirtilen ana bilgisayar ve bağlantı noktasında yazıcının başlatıldığını bildiren bir ileti almalısınız.

        ![Yazıcı öykünücüsü uygulaması yeniden açıldı.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Bu örnekte kullanılan yazıcı öykünücüsü uygulaması, etiketleri işlemek için bir web hizmetine bağlı olduğu için, güvenlik ayarlarınızın hizmetle iletişim kurmanıza izin verecek şekilde ayarlayın. Aksi takdirde, uygulama işlenmiş etiketleri almaz ve bu etiketlerin önizlemesi kullanılamaz.

### <a name="add-and-configure-a-local-printer"></a>Yerel yazıcı ekleme ve yapılandırma

Geçerli cihazın, oluşturulan etiketleri DRA'dan yazıcı öykünücü uygulamasına geçirmek için kullanabileceği [yeni bir yerel yazıcı ekleyin](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b).

1. Windos'ta; **Başlat** \> **Ayarlar** \> **Cihazlar** \> **Yazıcılar \& tarayıcılar**'ı seçin.
2. **Yazıcılar \& tarayıcılar ayarları**'nı seçin.
3. **Yazıcı veya tarayıcı ekle** için, **Cihaz ekle**'yi seçin.
4. **İstediğim yazıcı listede yok** için, **Manuel olarak ekle**'yi seçin.
5. **Diğer seçeneklere göre yazıcı bul** alanında, **El ile yapılan ayarlarla bir yerel yazıcı veya ağ yazıcısı ekle**'yi seçin.
6. **Yazıcı bağlantı noktası seç** alanında, **Yeni bağlantı noktası oluştur** öğesini seçin ve aşağıdaki adımları izleyin:

    1. **Bağlantı noktası türü** alanında, **Standart TCP/IP bağlantı noktası** seçeneğini belirleyin.
    2. **Ana bilgisayar adı veya IP adresi** alanına **127.0.0.1** girin.
    3. **Bağlantı noktası adı** alanına **ZPL** girin.
    4. **TCP/IP bağlantı noktası algılama** işlemi tamamlanana kadar bekleyin.
    5. **Cihaz türü** alanında, **Özel**'i ve ardından **Ayarlar**'ı seçin.
    6. Aşağıdaki bağlantı noktası ayarlarının belirtildiğinden emin olun:

        - **Bağlantı noktası adı:** ZPL
        - **Yazıcı adı veya IP adresi:** 127.0.0.1
        - **Protokol:** Ham
        - **Bağlantı noktası numarası:** 9100

7. **Yazıcı sürücüsünü yükle** alanında, **Genel/Yalnızca metin**'i seçin.
8. **Yazıcı adı** alanında, **ZebraPrinter** girin.

![Geçerli aygıt için yerel yazıcı ekleme.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA'ı yükleyin ve yapılandırın

Finance'teki oluşturulan etiketleri yapılandırılmış yerel yazıcıya geçirmek için DRA'yı hazırlayın.

1. [DRA'yı yükleme](install-document-routing-agent.md#install-the-document-routing-agent).
2. [DRA yapılandırma](install-document-routing-agent.md#configure-the-document-routing-agent).
3. DRA'da [yerel yazıcıyı kaydedin](install-document-routing-agent.md#register-network-printers).
4. Finance ortamında [yerel yazıcıyı etkinleştirin](install-document-routing-agent.md#administer-network-printers).

![Oluşturulan etiketlerin yazdırılması için DRA hazırlığı yapılıyor.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>ER hedefini yapılandırma

Finance'teki oluşturulan etiketleri DRA'ya geçirmek için ER hedefini hazırlayın.

1. Sırasıyla **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama hedefi** seçimlerini yapın.
2. **Elektronik raporlama hedefi** sayfasındaki Eylem Bölmesi'nde **Yeni**'yi seçin.
3. **Referans** alanında **Ambar konum etiketleri**'ni seçin.
4. **Dosya hedefi** hızlı sekmesinde **Yeni**'yi seçin.
5. **Ad** alanına, **Etiketler** yazın.
6. **Dosya bileşeni adı** alanında **Rapor**'u seçin.
7. **Ayarlar**'ı seçin.
8. **Hedef ayarları** iletişim kutusundaki **Yazıcı** sekmesinde **Etkin** seçeneğini **Evet** olarak ayarlayın.
9. **Yazıcı adı** alanında, **ZebraPrinter**'ı seçin.
10. **Belge yönlendirme türü** alanında **ZPL**'yi seçin.
11. **Tamam**'ı seçin.

![Elektronik raporlama hedef sayfasındaki Ambar konum etiketleri biçimi için ER hedefini yapılandırma.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Ambar konumlarını gözden geçirme

1. **Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Konumlar** öğesine gidin.
2. **Konumlar** sayfasında, yalnızca **Çek basamakları** alanında değeri olan yerleşimleri görmek için filtre uygulayın.

![Yerleşimler sayfasındaki ambar yerleşimlerini gözden geçirme.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Ambar konum etiketlerini yazdırma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ambar modeli**'ni genişletin ve **Ambar konum etiketleri**'ni seçin.
3. Eylem Bölmesinde, **Çalıştır**'ı seçin.
4. **Elektronik rapor parametreleri** iletişim kutusunda, **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin.
5. **Aralık** sekmesinde, **Tablo** alanının **Konumlar** olarak ve **Saha** alanının **Konum** olarak ayarlandığı satırı bulun. **Ölçütler** alanına **LPEnabled** girin.
6. **Tamam**'ı seçin.
7. **Tamam**'ı seçin. Bir etiket oluşturulur ve yazıcı öykünücüsü uygulamasındaki önizleme sayfasında gösterilir.

![Zpl Yazıcı öykünücüsü uygulamasının önizleme sayfasında oluşturulmuş bir etiketi görüntüleme.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Etiket yerleşimini değiştirme

Ambar konumu etiketlerinizin geçerli yerleşimini değiştirebilirsiniz. Aşağıdaki örnek, oluşturulan etiketlerin konum profil kimliği içerecek şekilde düzenin nasıl değiştirileceğini gösterir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Taslak durumu için hedefleri kullan** [ER kullanıcı parametresi](electronic-reporting-destinations.md#applicability)'ni **Evet** olarak ayarlayın.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ambar modeli**'ni genişletin ve **Ambar konum etiketleri**'ni seçin.
4. **Tasarımcı**’yı seçin.
5. **Biçim tasarımcısı** sayfasında, **Eşleme** sekmesinde `model.Location.Label` veri kaynağını seçin.
6. **Veri kaynağı özellikleri** iletişim kutusunda **Düzenle** \> **Formülü düzenle**'yi seçin.
7. **Formül tasarımcısı** sayfasında, **Formül** alanında, etiket oluşturmak için kullanılan ER formülünü gözden geçirin.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Oluşturulan etiketlere bir yerleşim profili kodu eklemek için formülü güncelleştirin.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. **Kaydet**'i seçin.
10. **Tamam**'ı seçin.
11. Eylem Bölmesinde, **Çalıştır**'ı seçin.
12. **Elektronik rapor parametreleri** iletişim kutusunda, **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin.
13. **Aralık** sekmesinde, **Tablo** alanının **Konumlar** olarak ve **Saha** alanının **Konum** olarak ayarlandığı satırı bulun. **Ölçüt** alanına, **Bölme** değerini girin.
14. **Tamam**'ı seçin.
15. **Tamam**'ı seçin. Bir etiket oluşturulur ve yazıcı öykünücüsü uygulamasındaki önizleme sayfasında gösterilir.

![Zpl Yazıcısı öykünücüsü uygulamasının önizleme sayfasındaki konum profil kimliğini içeren bir oluşturulmuş etiketi inceleme.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kodlama

> [!NOTE]
> Düzenlenebilir ER biçiminin **Ortak\\Dosya** bileşeninin kodlama ayarını ve hedef etiketin uygun ayarını eşitlemeniz gerekir. **Ortak\\Dosya** bileşeninin **[Kodlama](er-suppress-bom-characters.md)** alanı değeri, etiketin kodlamasını kontrol etmek için kullanılan bir ZPL komutu (örneğin `^CI` komutu) ile çelişmemelidir. ER, bu ayarların eşitlendiğini doğrulamaz.

## <a name="additional-resources"></a>Ek kaynaklar

[Yazıcı hedefi](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
