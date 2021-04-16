---
title: Elektronik raporlama sırasında oluşturulan büyük belgeleri sıkıştırma
description: Bu konu, Elektronik raporlama (ER) biçimi tarafından oluşturulan büyük belgelerin nasıl sıkıştırılacağını açıklamaktadır.
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: cd056798773bce492e429f8cca2ef39cb59bf739
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753828"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Elektronik raporlama sırasında oluşturulan büyük belgeleri sıkıştırma 

[!include [banner](../includes/banner.md)]

[Elektronik raporlama (ER) çerçevesini](general-electronic-reporting.md), giden belge oluşturmak üzere hareketlere ait verileri getiren bir çözüm yapılandırmak için kullanabilirsiniz. Oluşturulan bu belge çok büyük olabilir. Bu tür bir belge oluşturulduğunda, dosyayı tutmak için [Uygulama Nesne Sunucusu (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) belleği kullanılır. Bir noktada, belgenin Microsoft Dynamics 365 Finance uygulamasından yüklenmesi gerekir. Şu anda ER tarafından oluşturulan tek bir belgenin boyutu en fazla 2 gigabayt (GB) ile sınırlıdır. Ek olarak, Finance indirilen dosyanın boyutunu 1 GB ile [sınırlandırır](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3). Bu nedenle, bu sınırlamaların aşılma olasılığını azaltan ve bir **Akış çok uzundu** veya **Aritmetik işlemde taşma veya yetersiz gelme** özel durumu alacağınız bir ER çözümü yapılandırmalısınız.

Bir çözüm yapılandırdığınızda, iç içe geçmiş öğelerin herhangi biri tarafından oluşturulan içeriği sıkıştırmak için **Klasör** türünün bir kök öğesini ekleyerek ER biçimini Operations tasarımcısında ayarlayabilirsiniz. Sıkıştırma işlemi "tam zamanında" çalışır, böylece yüklenecek en yüksek bellek kullanımı ve dosya boyutu da azaltılabilir.

> [!NOTE]
> Dosya sıkıştırması, CPU kullanımının ek bir yüzdesini alır.

Bu yaklaşım hakkında daha fazla bilgi için bu konudaki örneği tamamlayın.

## <a name="example-compress-an-outbound-document"></a>Örnek: giden belgeyi sıkıştırma

Bu örnekte, **Sistem yöneticisi** veya **Elektronik raporlama işlev danışmanı** rolüne atanan bir kullanıcının oluşturulmuş bir belgeyi sıkıştırmak için bir ER biçimini nasıl yapılandırabileceği gösterilir.

### <a name="prerequisites"></a>Önkoşullar

Bu konudaki yordamları tamamlayabilmek için önce aşağıdaki adımları tamamlamanız gerekir.

1. [Yapılandırma sağlayıcısı etkinleştirin](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Örnek ER yapılandırmalarını içe aktarma](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [İçe aktarılan biçimi gözden geçirme](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Şu anda, biçim yapısı **Dosya** türünün **Rapor** öğesinden başlar ve XML öğeleri içerir. Bu nedenle, giden belge XML biçiminde oluşturulur ve sıkıştırma kullanılmaz.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Sıkıştırılmamış bir belge almak için ER biçimi oluşturma

1. [İçe aktarılan biçimi çalıştırma](er-defer-xml-element.md#run-the-imported-format).
2. XML biçiminde oluşturulan belgenin boyutunun 3 kilobayt (KB) olduğunu unutmayın.

    ![Sıkıştırılmamış giden belgenin önizlemesi](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Oluşturulan çıktıyı sıkıştırmak için biçimi değiştirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki yapılandırma ağacında, **Ertelenmiş öğeleri öğrenme modeli**'ni genişletin.
3. **Ertelenmiş XML öğelerini öğrenmek için biçimlendirme** yapılandırmasını seçin.
4. Biçim yapısını değiştirmek için **Tasarımcı**'yı seçin.
5. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde kök ögesini eklemek için **Kök ekle**'yi seçin.
6. **Ekle** iletişim kutusunda **Ortak\\Klasör**'ü seçin.
7. Yeni kök öğenin eklenmesini onaylamak için **Tamam**'ı seçin.
8. **Kaydet**'i seçin.

> [!NOTE]
> Biçim yapısı, **Klasör** türünün öğesinden başlar. Bu öğe, çıktıyı sıkıştırılmış (zip) dosya olarak oluşturur. **Rapor** öğesi tarafından oluşturulan bir belge giden bir ZIP dosyasına konulduğu zaman giden dosyanın boyutunu azaltmak için içeriği sıkıştırılır.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Sıkıştırılmış bir belge almak için ER biçimi oluşturma

1. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
2. Web tarayıcısının sunduğu zip dosyasını indirin ve incelemek üzere açın.
3. ZIP biçiminde oluşturulan belgenin boyutunun 1 KB olduğunu unutmayın.

    > [!NOTE] 
    > Bu zip dosyasının tuttuğu XML dosyasının sıkıştırma oranı yüzde 87'dir. Sıkıştırma oranı sıkıştırılan verilere bağlıdır.

    ![Sıkıştırılmış giden belgenin önizlemesi](./media/er-compress-outbound-files2.png)

> [!NOTE]
> ER [hedefi](electronic-reporting-destinations.md), çıktı üreten biçim öğesi (bu örnekteki **Rapor** öğesi) için yapılandırılmışsa, çıktının sıkıştırması atlanır.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)

[ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]