---
title: Satırları aynı Excel sayfasında birlikte tutmak için ER biçimi tasarlama
description: Bu makalede, aynı Microsoft Excel sayfasında satırları bir arada tutan Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı açıklanmaktadır.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287973"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Satırları aynı Excel sayfasında birlikte tutmak için ER biçimi tasarlama

[!include [banner](../includes/banner.md)]


Bu makalede, Sistem Yöneticisi veya Elektronik Raporlama İşlevsel Danışmanı rolündeki kullanıcıların Microsoft Excel'de giden belgeler oluşturan ve oluşturulan satırların aynı sayfada kalmasını sağlayan belge sayfalandırma yönetimini sunan [Elektronik Raporlama (ER)](general-electronic-reporting.md) [biçiminin](er-overview-components.md#format-component) nasıl oluşturulabileceği açıklanmaktadır.

Bu örnekte, Excel'de serbest metin faturalarını yazdırmak için kullanılan Microsoft tarafından sağlanan ER biçimini değiştirirsiniz. Değişiklikleriniz, oluşturulan serbest metin faturası raporunun sayfalandırmasını yönetmenizi sağlayacak ve böylece tek bir fatura satırının tüm satırları mümkün olduğunda aynı sayfada depolamasına imkan tanıyacak.

Bu makaledeki yordamlar **USMF** şirketinde tamamlanabilir. Kodlama gerekmez.

Bu örnekte, **Litware, Inc.** örnek şirketi için gerekli ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) oluşturacaksınız. **Litware, Inc.** (`http://www.litware.com`) örnek şirketinin yapılandırma sağlayıcısının ER çerçevesinde listelendiğinden ve **Etkin** olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısı listede yoksa veya **Etkin** olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

## <a name="enter-a-new-free-text-invoice"></a>Yeni bir serbest metin faturası girin

1. Serbest metin faturası eklemek için [Serbest metin faturası ekleme](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) bölümündeki adımları izleyin.

    1. Faturaya tek bir satır ekleyin.
    2. Fatura satırı için beş not ekleyin.

    ![Ekler sayfasındaki fatura satırı notlarını gözden geçirme.](./media/er-keep-excel-rows-together-notes.png)

2. Önceki adımda eklediğiniz fatura satırını kopyalayan beş ek fatura satırı oluşturmak için [Satırları kopyalama](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) alanındaki adımları izleyin.

    ![Serbest metin faturası sayfasındaki serbest metin faturası satırlarını gözden geçirme.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. Standart ER biçiminin özel bir sürümünü tasarlamak için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

## <a name="import-the-standard-er-format-configuration"></a>Standart ER biçimi yapılandırmasını içeri aktarma

Standart ER yapılandırmalarını Dynamics 365 Finance kurulumunuza eklemek için [Standart ER biçimi yapılandırmasını içeri aktarma](er-quick-start2-customize-report.md#ImportERSolution1) bölümündeki adımları izleyin. Örneğin, **Serbest metin faturası (Excel)** biçim yapılandırmasının **252.116** sürümünü içe aktarın. Temel **Fatura modeli** yapılandırmasının temel sürümü **252**, otomatik olarak gerekli **Fatura model eşleme** yapılandırmasıyla birlikte depodan içe aktarılır.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Yazdırma yönetimini standart ER biçimini kullanacak şekilde ayarlama

Standart ER biçiminin serbest metin faturaları yazdırmak için kullanılabilmesi için **Alacak hesapları** modülü için yazdırma yönetimini yapılandırmak üzere [Yazdırma yönetimini ayarlama](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) bölümündeki adımları izleyin.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Standart ER biçimi için biçim hedefi konfigüre etme

Oluşturulan raporların PDF biçimine dönüştürülmesi ve yeni tarayıcı sekmesinde önizlenmesi için standart ER biçiminin [Ekran](er-destination-type-screen.md) ER hedefini yapılandırmak üzere [Ekrandaki önizleme için biçim hedefini yapılandırma](er-quick-start1-new-solution.md#ConfigureDestination) bölümündeki adımları izleyin.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Standart ER biçimini kullanarak serbest metin faturası yazdırma

1. Eklenen fatura için Excel biçiminde serbest metin faturası oluşturmak üzere standart ER biçimini kullanmak için [Serbest metin faturası yazdırma](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) bölümündeki adımları izleyin.
2. Oluşturulan Excel çalışma kitabını indirin ve Excel masaüstü uygulamasında gözden geçirin.

    Faturanın altıncı satırının raporun ilk sayfasında başlayacağını ve ikinci sayfada devam edeceğini unutmayın. İkinci sayfada son not görünür ve altıncı fatura satırına ait olduğu çok belli olmaz. Bu nedenle, fatura satırına ilişkin içeriğin ortasındaki sayfa sonu, bu belgenin okunmasını zorlaştırır.

    ![Oluşturulan serbest metin faturasının sayfalandırmasını, Excel masaüstü uygulamasında gözden geçirme.](./media/er-keep-excel-rows-together-invoice1.gif)

Bu makaledeki geri kalan yordamlar, aynı sayfadaki tek bir fatura satırı için tüm içeriği saklayarak, fatura raporunun görünümünü ve okunabilirliğini iyileştirmek için standart ER biçimini nasıl ayarlayabileceğinizi gösterir.

## <a name="create-a-custom-format"></a>Özel biçim oluşturma

İçe aktarılan ER biçiminden bir biçim türetmek ve düzenleme ve değiştirme yapılabilir bir **Serbest metin faturası (Excel) özel** ER yapılandırması oluşturmak üzere [Özel biçim oluşturma](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) bölümündeki adımları izleyin.

## <a name="edit-the-custom-format"></a>Özel biçimi düzenleme

1. ER biçim tasarımcısında türetilen ER biçimini açmak üzere [Özel biçim oluşturma](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) bölümündeki adımları izleyin.
2. **Biçim tasarımcısı** sayfasında, sol bölmedeki biçim bileşen ağacında, **Serbest metin faturası \> Sayfa \> InvoiceLines** bölümünü genişletin ve **InvoiceLines_Values** bileşenini seçin.
3. **Biçim** sekmesinde, **Satırları beraber tut** seçeneğini **Evet** olarak ayarlayın.

    ![Biçim tasarımcısı sayfasında, düzenlenebilir ER biçimi için Satırları beraber tut seçeneğini ayarlama.](./media/er-keep-excel-rows-together-format.png)

4. **Kaydet**'i seçip sayfayı kapatın.

## <a name="mark-the-custom-format-as-runnable"></a>Özel biçimi çalıştırılabilir olarak işaretleme

Özel ER biçiminin değiştirilmiş sürümünü çalıştırılabilir yapmak için [Özel biçimi çalıştırılabilir olarak işaretleme](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) bölümündeki adımları izleyin.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Yazdırma yönetimini özel ER biçimini kullanacak şekilde ayarlama

Özel ER biçiminin serbest metin faturaları yazdırmak için kullanılabilmesi için **Alacak hesapları** modülü için yazdırma yönetimini yapılandırmak üzere [Yazdırma yönetimini ayarlama](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) bölümündeki adımları izleyin.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Özel ER biçimi için biçim hedefi konfigüre etme

Oluşturulan raporların PDF biçimine dönüştürülmesi ve yeni tarayıcı sekmesinde önizlenmesi için özel ER biçiminin **Ekran** ER hedefini yapılandırmak üzere [Ekrandaki önizleme için biçim hedefini yapılandırma](er-quick-start1-new-solution.md#ConfigureDestination) bölümündeki adımları izleyin.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Özel ER biçimini kullanarak serbest metin faturası yazdırma

1. Eklenen fatura için Excel biçiminde serbest metin faturası oluşturmak üzere özel ER biçimini kullanmak için [Serbest metin faturası yazdırma](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) bölümündeki adımları izleyin.
2. Oluşturulan Excel çalışma kitabını indirin ve Excel masaüstü uygulamasında gözden geçirin.

    Faturanın altıncı satırının ikinci sayfada başlayacağını ve bu fatura satırını temsil eden tüm Excel satırları ilgili sayfada birlikte göründüğünü unutmayın.

    ![Oluşturulan serbest metin faturasının güncelleştirilmiş sayfalandırmasını, Excel masaüstü uygulamasında gözden geçirme.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Ek kaynaklar

[Excel biçiminde belgeler oluşturmak için yapılandırma tasarlama](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
