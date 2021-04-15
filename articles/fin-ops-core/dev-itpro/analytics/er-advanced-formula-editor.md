---
title: Elektronik raporlama gelişmiş formül düzenleyicisi
description: Bu konu, Elektronik raporlama (ER) model eşlemesi ve biçim bileşenlerinde ifade yapılandırmak için, gelişmiş formül düzenleyicinin nasıl kullanılabileceğini açıklamaktadır.
author: NickSelin
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751220"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Elektronik raporlama gelişmiş formül düzenleyicisi

[!include [banner](../includes/banner.md)]

[Elektronik raporlama](general-electronic-reporting.md) [formül düzenleyicisine](general-electronic-reporting-formula-designer.md) ek olarak, Elektronik raporlama (ER) ifadelerini yapılandırma deneyimini geliştirmek için gelişmiş Elektronik raporlama formül düzenleyicisini de kullanabilirsiniz. Gelişmiş düzenleyici, [Monaco editor](https://microsoft.github.io/monaco-editor) tarafından sunulan, tarayıcı tabanlı ve güçlü bir düzenleyicidir. En sık kullanılan gelişmiş düzenleyici özellikleri bu konuda açıklanmaktadır:

- [Kodu otomatik biçimlendirme](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Kod tamamlama](#CodeCompletion)
- [Kod gezintisi](#CodeNavigation)
- [Kod yapılandırma](#CodeStructuring)
- [Bul ve değiştir](#FindAndReplace)
- [Veri yapıştırma](#DataPasting)
- [Sözdizimi renklendirme](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Gelişmiş formül düzenleyicisini etkinleştirme</a>

Microsoft Dynamics 365 Finance kurulumunuzda gelişmiş formül düzenleyicisini kullanmaya başlamak için aşağıdaki adımları tamamlayın.

1.  **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2.  **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3.  **Kullanıcı parametreleri** iletişim kutusunun **Yürütme izleme** bölümünde **Gelişmiş formül düzenleyicisini etkinleştir** parametresini **Evet** olarak ayarlayın.

[![ER yapılandırma sayfası](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Bu parametrenin kullanıcıya özel ve şirkete özel olduğuna dikkat edin.

## <a name=""></a><a name="Autoformatting">Kodu otomatik biçimlendirme</a>

Birden fazla kod satırı içeren karmaşık bir ifade yazdığınız zaman, yeni bir girilen satırın girintilemesi önceki satırın girintilemesine göre otomatik olarak yapılır. Satırları seçip girintilemelerini **Sekme**'ye veya **Üst Krkt+Sekme** tuşlarına basarak değiştirebilirsiniz.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Otomatik biçimlendirme, bakımı ve yapılandırılan mantığın anlaşılmasını kolaylaştırmak için tüm ifadeyi iyi biçimlendirilmiş durumda tutmanıza olanak sağlar.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Düzenleyici, ifadeyi daha hızlı yazmanıza ve yazım hatalarını önlemenize yardımcı olmak için sözcük tamamlama sağlar. Yeni metin eklemeye başladığınızda, düzenleyici, girdiğiniz karakterleri içeren ER işlevlerinde desteklenen işlevlerin bir listesini otomatik olarak sunar. Yapılandırılmış bir ifadenin herhangi bir yerinde **Ctrl + Boşluk** tuşlarına basarak IntelliSense'i de tetikleyebilirsiniz.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kod tamamlama</a>

Düzenleyici aşağıdaki eylemlerle kodun otomatik olarak tamamlanmasını sağlar:

- Açma ayracı girilince bir kapatma ayracı girip, imleci ayraçların içinde tutarak.
- İlk tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.
- İlk çift tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Yazılan ayracın üzerine geldiğinizde, bu çiftin ikinci ayracı, destekledikleri yapıyı gösterecek şekilde otomatik olarak vurgulanır.

## <a name=""></a><a name="CodeNavigation">Kod gezintisi</a>

Komut paletini veya bağlam menüsünü kullanıp **Go to** komutunu yazarak ifadenizde gerekli sembolleri veya çizgileri bulabilirsiniz.

Örneğin, **8**. satıra atlamak için aşağıdakileri yapın:

- **Ctrl + G** tuşlarına basın, **8** değerini girin ve **Enter** tuşuna basın.

  -veya-

- **F1** tuşuna basın, **G** yazın, **Go to line**'ı seçin, **8** değerini girin ve **Enter** tuşuna basın.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Kod yapılandırma</a>

[IF](er-functions-logical-if.md) veya [CASE](er-functions-logical-case.md) gibi bazı işlevlerin kodu otomatik olarak yapılandırılır. Yalnızca ilgilenmeniz gereken kod parçasına odaklanmak için, bir ifadenin düzenlenebilen kısmını küçültmek üzere bu kodun katlama bölgelerini genişletebilir veya daraltabilirsiniz. Bunun için katla/aç geçişi kullanılabilir.

Örneğin tüm bölgeleri katlamak için aşağıdakileri yapın:

- **Ctrl+K** tuşlarına basın

  -veya-

- **F1**'e basın, **FO**'ya basın, **Tümünü katla**'yı seçin ve **Enter**'a basın

Tüm bölgeleri açmak için aşağıdakileri yapın:

- **Ctrl+J** tuşlarına basın

  -veya-
  
- **F1**'e basın, **UN** yazın, **Tümünü aç**'ı seçin ve **Enter**'a basın

[![ER formül düzenleyicisi](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Bul ve değiştir</a>

Belirli bir metnin yinelemelerini bulmak için, ifadenizde metni seçin ve aşağıdakileri yapın:

- Seçili metnin bir sonraki yinelemesini bulmak için **Ctrl + F** ve ardından **F3** tuşlarına basın veya önceki yinelemeyi bulmak için **Shift + F3** tuşlarına basın.

  -veya-
  
- **F1** tuşuna basın, **F** yazın ve seçili metni bulmak için gerekli seçeneği belirleyin.

Belirli bir metnin yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:

- **Ctrl+H** tuşlarına basın. Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.

  -veya-
  
- **F1** tuşuna basın, **R** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin. Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.

Belirli bir metnin tüm yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:

- **Ctrl + F2** tuşlarına basın ve ardından alternatif metni girin.

  -veya-
  
- **F1** tuşuna basın, **C** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin. Alternatif metni girin.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Veri kaynaklarını ve işlevleri yapıştırma</a>

**Veri kaynağı** sol bölmesinde seçili olan bir veri kaynağını geçerli ifadeye yapıştırmak için **Veri kaynağı ekle**'yi seçebilirsiniz. Benzer şekilde, **İşlevler** sağ bölmesinde seçili olan bir işlevi geçerli ifadeye yapıştırmak için **İşlev ekle**'yi seçebilirsiniz. ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı yapılandırılan ifadenin hep sonuna yapıştırılır. Gelişmiş ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı, yapılandırılan ifadenin herhangi bir yerine yapıştırılır. Verileri yapıştırmak istediğiniz yeri belirtmek için imleci kullanmanız gerekir.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Sözdizimi renklendirme</a>

Şu anda, ifadelerin aşağıdaki kısımlarını vurgulamak için farklı renkler kullanılıyor:

- Bir metin sabitinin etiket kodunu temsil edebilen, ayraç içindeki metin.

[![ER formül düzenleyicisi](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Sınırlamalar

Düzenleyici şu anda aşağıdaki web tarayıcılarında desteklenmektedir:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)
- [Monaco editor](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]