---
title: Her tüzel kişilik için ER biçiminin parametrelerini ayarlama
description: Bu konu, her tüzel kişilik için bir Elektronik raporlama (ER) biçimi parametrelerini nasıl ayarlayabileceğinizi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681484"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Her tüzel kişilik için ER biçiminin parametrelerini ayarlama

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Önkoşullar

Bu adımları tamamlamak için önce [Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md) konusundaki adımları tamamlamanız gerekir.

Bu konudaki örnekleri tamamlamak üzere aşağıdaki rollerden biri için Microsoft Dynamics 365 Finance'e (Finance) erişiminiz olmalıdır:

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

## <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın

1.  Ortamınızda oturum açın.
2.  Varsayılan panoda **Elektronik raporlama**'yı seçin.
3.  **Raporlama yapılandırmaları**'nı seçin.
4.  [Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md) konusundaki adımları tamamlarken Regulatory Configuration Services (RCS) aracından dışa aktardığınız yapılandırmaları Finance uygulamasının geçerli kurulumuna içe aktarın. Her Elektronik raporlama (ER) yapılandırması için aşağıdaki adımları takip edin: veri modeli, model eşleme ve biçimler.

    1. **Değişim \> XML dosyasından yükle**'yi seçin.
    2. Gerekli ER yapılandırması için XML biçimindeki dosyayı seçmek üzere **Gözat**'ı seçin.
    3. **Tamam**'ı seçin.
    
    Aşağıdaki şekil, tamamladığınızda sahip olmanız gereken yapılandırmaları gösterir.

    ![ER yapılandırma sayfası](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>DEMF şirketi için parametreleri ayarlama

ER biçimi için uygulamaya özel parametreleri ayarlamak üzere ER çerçevesini kullanabilirsiniz.

1.  **DEMF** tüzel kişiliğini seçin.
2.  Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.
3.  Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm.PNG)
    
    **Uygulama özel parametreleri** sayfasında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçiminin **Seçici** veri kaynağı için kuralları yapılandırabilirsiniz.
    
    Temel ER biçimi, **Arama** türünde birkaç veri kaynağı içerecekse veri kaynağı için kurallar kümesini yapılandırmaya başlamadan önce **Aramalar** hızlı sekmesinde istediğiniz veri kaynağını seçmelisiniz.
    
    Her veri kaynağı için seçilen ER biçiminin her sürümüne ayrı kurallar yapılandırabilirsiniz.
    
    Temel ER biçiminin seçilen sürümünde var olan tüm arama veri kaynakları için kuralların tamamı, ER biçiminin uygulama özel parametrelerini oluşturur.

4.  ER biçiminin **1.1.1** sürümünü seçin.
5.  **Koşullar** hızlı sekmesinde **Ekle**'yi seçin.
6.  Yeni kaydın **Kod** alanında aramayı açmak için açılır oku seçin.

    Arama, seçim için vergi kodlarının bir listesini gösterir. Bu liste, temel ER biçiminde yapılandırılmış **Model.Data.Tax** veri kaynağı tarafından döndürülür. Bu veri kaynağı **Ad** alanını içerdiğinden her vergi kodunun adı aramada görünür.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  **VAT19** vergi kodunu seçin.
8.  Yeni kaydın **Arama sonucu** alanında aramayı açmak için açılır menü okunu seçin. Arama, seçimin TaxationLevel biçim numaralandırması için değerlerin listesini gösterir.

    Oturum açtığınız kullanıcının tercih ettiği dil olarak Almanca seçiliyse aramadaki değerlerin etiketlerinin temel ER biçiminde çevrilmiş olmaları koşuluyla Almanca olacağını unutmayın. Ek olarak, bir arama veri kaynağının etiketi çevrilmişse bu etiket kullanıcının **Aramalar** sekmesinde tercih ettiği dilde görünür.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  **Normal vergilendirme** değerini seçin.

    Bu kaydı ekleyerek aşağıdaki kuralı tanımlarsınız: **Seçici** arama veri kaynağı talep edildiğinde ve **VAT19** vergi kodu bir bağımsız değişken olarak iletildiğinde istenen vergi seviyesi olarak **Normal vergilendirme** geri döndürülür.

10. **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **InVAT19** vergi kodunu seçin.
    2. **Arama sonuçları** alanında **Normal vergilendirme** değerini seçin.
    
11. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **VAT7** vergi kodunu seçin.
    2. **Arama sonuçları** alanında **Azaltılmış vergilendirme** değerini seçin.
    
12. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **InVAT7** vergi kodunu seçin.
    2. **Arama sonuçları** alanında **Azaltılmış vergilendirme** değerini seçin.
    
13. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **THIRD** vergi kodunu seçin.
    2. **Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.
    
14. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **InVAT0** vergi kodunu seçin.
    2. **Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.
    
15. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Kod** alanında **\*Boş değil\*** seçeneğini belirleyin.
    2. **Arama sonuçları** alanında **Diğer** değerini seçin.
    
    Bu son kaydı ekleyerek aşağıdaki kuralı tanımlarsınız: Bağımsız değişken olarak geçirilen vergi kodu önceki kuralların herhangi birini karşılamadığında arama veri kaynağı istenen vergilendirme düzeyi olarak **Diğer** değerini döndürür.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. **Durum** alanında **Tamamlandı**'yı seçin.

    **Tamamlandı** veya **Paylaşılan** durumuna sahip bir ER biçimi sürümü çalıştırdığınızda bu kurallar kümesinin **Tamamlandı** durumunda olması gerekir. Aksi takdirde, **Seçici** arama veri kaynağı çalıştırılırken biçim, bu kurallar grubundan veri yüklemeye çalıştığında temel ER biçiminin yürütülmesi kesintiye uğrar.
    
    **Taslak** durumuna sahip bir ER biçimi sürümü çalıştırdığınızda temel ER biçimi, durumundan bağımsız olarak bu kurallara erişebilir.
    
17. **Kaydet**'i seçin.
18. **Uygulama özel parametreleri** sayfasını kapatın.

## <a name="run-the-er-format-in-the-demf-company"></a>DEMF şirketinde ER biçimini çalıştırma

1.  Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.
2.  Eylem Bölmesinde, **Çalıştır**'ı seçin.
3.  Görünen iletişim kutusunda **Tamam**'ı seçin.
4.  Oluşturulan açıklamayı karşıdan yükleyin ve yerel olarak saklayın.

    Oluşturulan açıklamada, **InVAT7** vergi kodunun özetinin **Azaltılmış** düzeye, **VAT19** ve **InVA19** vergi kodlarının özetlerinin **Normal** düzeye getirildiğine dikkat edin. Bu davranış, tüzel kişiliğe bağlı kurallar kümesindeki yapılandırma tarafından belirlenir.
    
5.  **Vergi \> Dolaylı vergiler \> Satış vergisi \> Satış vergisi kodları**'na gidin.
6.  **InVAT7** vergi kodunu seçin.
7.  Vergi değeri ve vergi kodu başına uygulanan vergi oranı hakkındaki bilgileri görüntülemek için Eylem Bölmesinde, **Satış vergisi kodu** sekmesinde, **Sorgular** grubunda, **Deftere nakledilen satış vergisi**'ni seçin.

    ![Deftere nakledilen satış vergisi sayfası](./media/GER-AppSpecParms-Statement.PNG)

8.  Deftere nakledilen satış vergisi sayfasını kapatın.

## <a name="set-up-parameters-for-the-usmf-company"></a>USMF şirketi için parametreleri ayarlama

1.  **USMF** tüzel kişiliğini seçin.
2.  **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
3.  Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin, **Parametreli çağrıları öğrenmek için biçimlendirme** öğesini genişletin ve **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.
4.  Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.
5.  Seçili ER biçiminin **1.1.1** sürümünü seçin.
6.  **Koşullar** hızlı sekmesinde **Ekle**'yi seçin.
7.  Yeni kaydın **Kod** alanında aramayı açmak için açılır oku seçin.

    Arama şimdi, yapılan seçim için **USMF** şirket vergisinin vergi kodlarının bir listesini sunar.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  **EXEMPT** vergi kodunu seçin.
9.  Yeni kaydın **Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.
10. Yeniden **Ekle**'yi seçin.
11. Yeni kaydın **Kod** alanında **\*Boş değil\*** seçeneğini belirleyin.
12. Yeni kaydın **Arama sonuçları** alanında **Normal vergilendirme** değerini seçin.
13. **Durum** alanında **Tamamlandı**'yı seçin.
14. **Kaydet**'i seçin.

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. **Uygulama özel parametreleri** sayfasını kapatın.

## <a name="run-the-er-format-in-the-usmf-company"></a>USMF şirketinde ER biçimini çalıştırma

1.  Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.
2.  Eylem Bölmesinde, **Çalıştır**'ı seçin.
3.  Görünen iletişim kutusunda **Tamam**'ı seçin.
4.  Oluşturulan açıklamayı karşıdan yükleyin ve yerel olarak saklayın.

    Oluşturulan açıklamada, şimdi ER biçiminde herhangi bir ayarlama yapmadan aynı ER biçimini farklı bir tüzel kişilik için tekrar kullandığınız belirtilmektedir.

## <a name="reuse-legal-entitydependent-parameters"></a>Tüzel kişiliye bağlı parametreleri yeniden kullanma

### <a name="export-parameters"></a>Parametreleri dışa aktarma

1.  **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.
2.  **Raporlama yapılandırmaları**'nı seçin.
3.  Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.
4.  Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.
5.  ER biçiminin **1.1.1** sürümünü seçin.
6.  Eylem Bölmesinde **Dışa aktar**'ı seçin.
7.  Oluşturulan dosyayı karşıdan yükleyin ve yerel olarak saklayın.

    Yapılandırılmış uygulamaya özel parametreler kümesi artık bir XML dosyası olarak dışa aktarıldı.

### <a name="import-parameters"></a>Parametreleri içe aktarma

1.  ER biçiminin **1.1.2** sürümünü seçin.
2.  Eylem Bölmesinde, **İçe aktar**'ı seçin.
3.  Bu biçim sürümü için var olan uygulamaya özel parametreleri geçersiz kılmak istediğinizi onaylamak üzere **Evet**'i seçin.
4.  **1.1.1** sürümü için dışa aktarılan uygulamaya özel parametreleri içeren dosyayı bulmak üzere **Gözat**'ı seçin.
5.  **Tamam**'ı seçin.

    ER biçiminin **1.1.2** sürümü, başlangıçta **1.1.1** sürümü için yapılandırdığınız uygulamaya özel parametrelere sahiptir.
    
    ER biçiminin uygulamaya özel parametrelerinin tüzel kişiliğe bağlı olduğunu unutmayın. Bir tüzel kişilik için yapılandırılmış olan uygulamaya özel parametreleri farklı bir tüzel kişilikte yeniden kullanmak için ilk tüzel kişilikte oturum açtığınızda bunları dışa aktarmalı ve diğer tüzel kişilikte oturum açtıktan sonra içe aktarmalısınız.

    Bu yaklaşımı, ilk olarak bir Finance kurulumunda yapılandırılmış olan uygulamaya özel parametreleri ER biçimiyle ilgili başka bir Finance kurulumuna aktarmak için de kullanabilirsiniz.

    ER biçiminin bir sürümü için uygulamaya özel parametreler yapılandırırsanız ve aynı biçimin daha yüksek bir sürümünü geçerli Finance kurulumuna içe aktarırsanız var olan uygulamaya özel parametrelerin, içe aktarılan sürüm için uygulanmayacağına dikkat edin.
    
    Ayrıca, içe aktarmak için bir dosya seçtiğinizde bu dosyadaki uygulamaya özel parametrelerin yapısının, içe aktarma için seçilen ER biçimindeki **Arama** türünde karşılık gelen veri kaynağının yapısıyla karşılaştırıldığını unutmayın. İçe aktarma, uygulamaya özel her parametrenin yapısı içe aktarma için seçilen ER biçiminde ilgili veri kaynağının yapısıyla eşleştiğinde gerçekleşir. Yapılar eşleşmezse içe aktarmanın yapılamadığını bildiren bir uyarı iletisi alırsınız. İçe aktarma işleminin yapılmasını zorlarsanız seçilen ER biçimi için uygulamaya özel var olan parametreler temizlenir ve bunları en baştan ayarlamanız gerekir.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Uygulamaya özel parametreler ile ER biçimi arasındaki ilişki

ER biçimi ile uygulamaya özel parametreler arasındaki ilişki, ER biçiminin kurulumdan bağımsız benzersiz tanımlama kodu ile kurulur. Bu nedenle, bir ER biçimini Finance'tan kaldırdığınızda ER biçimi için yapılandırılmış olan uygulamaya özel parametreler geçerli Finance kurulumunda tutulur. Temel ER biçimi, bu Finance kurulumuna yeniden içe aktarıldığında bunlara erişilebilir.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>ER çerçevesini kullanarak uygulamaya özel parametrelere erişme

Önceki örnekte, ER çerçevesini kullanarak ER biçimindeki uygulamaya özel parametrelere eriştiniz. Bu yaklaşım, belirli bir ER biçiminin uygulamaya özel parametrelerine erişimi kısıtlamanıza izin vermez. Bu tür kısıtlamalar uygulamanız gerekiyorsa aşağıdaki adımları izleyin. 

1.  Var olan bir **ERSolutionAppSpecificParametersDesigner** menü öğesini yeniden kullanın veya kendi **ERSolutionAppSpecificParametersDesigner** menü öğenizi uygulayın.

    ![Visual Studio sayfası](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Şu adımlardan birini izleyin:

    1.  Yeni bir menü öğesi düğmesi oluşturun ve **Veri Kaynağı** özelliğini **ERSolutionTable** olarak ayarlayarak **ERSolutionTable** tablosundan ilgili kayda bağlayın.
    
        ![Visual Studio sayfası](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Basit bir düğme oluşturun ve aşağıdaki örnekte gösterildiği gibi **Tıklandı** yöntemini geçersiz kılın.
    
        Bu yaklaşımı kullanarak, yalnızca belirli bir ER biçiminin ve ondan türetilmiş alt öğe kopyalarının uygulamaya özel parametrelerine erişim izni vermek için (**GUID** değeri ile tanımlanmış) benzersiz bir çözüm kimliği belirleyebilirsiniz.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md)
