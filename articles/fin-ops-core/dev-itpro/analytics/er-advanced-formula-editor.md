---
title: Elektronik raporlama gelişmiş formül düzenleyicisi
description: Bu konu, Elektronik raporlama (ER) model eşlemesi ve biçim bileşenlerinde ifade yapılandırmak için, gelişmiş formül düzenleyicinin nasıl kullanılabileceğini açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 14eb8a59b64a49649768f93befdf8e6e8dcf8105
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685395"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="f2765-103">Elektronik raporlama gelişmiş formül düzenleyicisi</span><span class="sxs-lookup"><span data-stu-id="f2765-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2765-104">[Elektronik raporlama](general-electronic-reporting.md) [formül düzenleyicisine](general-electronic-reporting-formula-designer.md) ek olarak, Elektronik raporlama (ER) ifadelerini yapılandırma deneyimini geliştirmek için gelişmiş Elektronik raporlama formül düzenleyicisini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="f2765-105">Gelişmiş düzenleyici, [Monaco editor](https://microsoft.github.io/monaco-editor) tarafından sunulan, tarayıcı tabanlı ve güçlü bir düzenleyicidir.</span><span class="sxs-lookup"><span data-stu-id="f2765-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="f2765-106">En sık kullanılan gelişmiş düzenleyici özellikleri bu konuda açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="f2765-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="f2765-107">Kodu otomatik biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="f2765-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="f2765-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="f2765-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="f2765-109">Kod tamamlama</span><span class="sxs-lookup"><span data-stu-id="f2765-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="f2765-110">Kod gezintisi</span><span class="sxs-lookup"><span data-stu-id="f2765-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="f2765-111">Kod yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f2765-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="f2765-112">Bul ve değiştir</span><span class="sxs-lookup"><span data-stu-id="f2765-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="f2765-113">Veri yapıştırma</span><span class="sxs-lookup"><span data-stu-id="f2765-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="f2765-114">Sözdizimi renklendirme</span><span class="sxs-lookup"><span data-stu-id="f2765-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="f2765-115"><a name="ActivateAdvEditor">Gelişmiş formül düzenleyicisini etkinleştirme</a></span><span class="sxs-lookup"><span data-stu-id="f2765-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="f2765-116">Microsoft Dynamics 365 Finance kurulumunuzda gelişmiş formül düzenleyicisini kullanmaya başlamak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f2765-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="f2765-117">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="f2765-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="f2765-118">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f2765-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="f2765-119">**Kullanıcı parametreleri** iletişim kutusunun **Yürütme izleme** bölümünde **Gelişmiş formül düzenleyicisini etkinleştir** parametresini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f2765-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="f2765-120">[![ER yapılandırma sayfası](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="f2765-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="f2765-121">Bu parametrenin kullanıcıya özel ve şirkete özel olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f2765-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="f2765-122"><a name="Autoformatting">Kodu otomatik biçimlendirme</a></span><span class="sxs-lookup"><span data-stu-id="f2765-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="f2765-123">Birden fazla kod satırı içeren karmaşık bir ifade yazdığınız zaman, yeni bir girilen satırın girintilemesi önceki satırın girintilemesine göre otomatik olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="f2765-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="f2765-124">Satırları seçip girintilemelerini **Sekme**'ye veya **Üst Krkt+Sekme** tuşlarına basarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="f2765-125">[![ER formül düzenleyicisi](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="f2765-126">Otomatik biçimlendirme, bakımı ve yapılandırılan mantığın anlaşılmasını kolaylaştırmak için tüm ifadeyi iyi biçimlendirilmiş durumda tutmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f2765-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="f2765-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="f2765-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="f2765-128">Düzenleyici, ifadeyi daha hızlı yazmanıza ve yazım hatalarını önlemenize yardımcı olmak için sözcük tamamlama sağlar.</span><span class="sxs-lookup"><span data-stu-id="f2765-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="f2765-129">Yeni metin eklemeye başladığınızda, düzenleyici, girdiğiniz karakterleri içeren ER işlevlerinde desteklenen işlevlerin bir listesini otomatik olarak sunar.</span><span class="sxs-lookup"><span data-stu-id="f2765-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="f2765-130">Yapılandırılmış bir ifadenin herhangi bir yerinde **Ctrl + Boşluk** tuşlarına basarak IntelliSense'i de tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="f2765-131">[![ER formül düzenleyicisi](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="f2765-132"><a name="CodeCompletion">Kod tamamlama</a></span><span class="sxs-lookup"><span data-stu-id="f2765-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="f2765-133">Düzenleyici aşağıdaki eylemlerle kodun otomatik olarak tamamlanmasını sağlar:</span><span class="sxs-lookup"><span data-stu-id="f2765-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="f2765-134">Açma ayracı girilince bir kapatma ayracı girip, imleci ayraçların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="f2765-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="f2765-135">İlk tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="f2765-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="f2765-136">İlk çift tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="f2765-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="f2765-137">[![ER formül düzenleyicisi](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="f2765-138">Yazılan ayracın üzerine geldiğinizde, bu çiftin ikinci ayracı, destekledikleri yapıyı gösterecek şekilde otomatik olarak vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="f2765-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="f2765-139"><a name="CodeNavigation">Kod gezintisi</a></span><span class="sxs-lookup"><span data-stu-id="f2765-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="f2765-140">Komut paletini veya bağlam menüsünü kullanıp **Go to** komutunu yazarak ifadenizde gerekli sembolleri veya çizgileri bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="f2765-141">Örneğin, **8**. satıra atlamak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="f2765-142">**Ctrl + G** tuşlarına basın, **8** değerini girin ve **Enter** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="f2765-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="f2765-143">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-143">-or-</span></span>

- <span data-ttu-id="f2765-144">**F1** tuşuna basın, **G** yazın, **Go to line**'ı seçin, **8** değerini girin ve **Enter** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="f2765-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="f2765-145">[![ER formül düzenleyicisi](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="f2765-146"><a name="CodeStructuring">Kod yapılandırma</a></span><span class="sxs-lookup"><span data-stu-id="f2765-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="f2765-147">[IF](er-functions-logical-if.md) veya [CASE](er-functions-logical-case.md) gibi bazı işlevlerin kodu otomatik olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="f2765-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="f2765-148">Yalnızca ilgilenmeniz gereken kod parçasına odaklanmak için, bir ifadenin düzenlenebilen kısmını küçültmek üzere bu kodun katlama bölgelerini genişletebilir veya daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="f2765-149">Bunun için katla/aç geçişi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f2765-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="f2765-150">Örneğin tüm bölgeleri katlamak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="f2765-151">**Ctrl+K** tuşlarına basın</span><span class="sxs-lookup"><span data-stu-id="f2765-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="f2765-152">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-152">-or-</span></span>

- <span data-ttu-id="f2765-153">**F1**'e basın, **FO**'ya basın, **Tümünü katla**'yı seçin ve **Enter**'a basın</span><span class="sxs-lookup"><span data-stu-id="f2765-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="f2765-154">Tüm bölgeleri açmak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="f2765-155">**Ctrl+J** tuşlarına basın</span><span class="sxs-lookup"><span data-stu-id="f2765-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="f2765-156">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-156">-or-</span></span>
  
- <span data-ttu-id="f2765-157">**F1**'e basın, **UN** yazın, **Tümünü aç**'ı seçin ve **Enter**'a basın</span><span class="sxs-lookup"><span data-stu-id="f2765-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="f2765-158">[![ER formül düzenleyicisi](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="f2765-159"><a name="FindAndReplace">Bul ve değiştir</a></span><span class="sxs-lookup"><span data-stu-id="f2765-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="f2765-160">Belirli bir metnin yinelemelerini bulmak için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="f2765-161">Seçili metnin bir sonraki yinelemesini bulmak için **Ctrl + F** ve ardından **F3** tuşlarına basın veya önceki yinelemeyi bulmak için **Shift + F3** tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="f2765-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="f2765-162">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-162">-or-</span></span>
  
- <span data-ttu-id="f2765-163">**F1** tuşuna basın, **F** yazın ve seçili metni bulmak için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f2765-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="f2765-164">Belirli bir metnin yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="f2765-165">**Ctrl+H** tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="f2765-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="f2765-166">Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f2765-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="f2765-167">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-167">-or-</span></span>
  
- <span data-ttu-id="f2765-168">**F1** tuşuna basın, **R** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f2765-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="f2765-169">Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f2765-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="f2765-170">Belirli bir metnin tüm yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="f2765-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="f2765-171">**Ctrl + F2** tuşlarına basın ve ardından alternatif metni girin.</span><span class="sxs-lookup"><span data-stu-id="f2765-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="f2765-172">-veya-</span><span class="sxs-lookup"><span data-stu-id="f2765-172">-or-</span></span>
  
- <span data-ttu-id="f2765-173">**F1** tuşuna basın, **C** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f2765-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="f2765-174">Alternatif metni girin.</span><span class="sxs-lookup"><span data-stu-id="f2765-174">Enter the alternative text.</span></span>

<span data-ttu-id="f2765-175">[![ER formül düzenleyicisi](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="f2765-176"><a name="DataPasting">Veri kaynaklarını ve işlevleri yapıştırma</a></span><span class="sxs-lookup"><span data-stu-id="f2765-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="f2765-177">**Veri kaynağı** sol bölmesinde seçili olan bir veri kaynağını geçerli ifadeye yapıştırmak için **Veri kaynağı ekle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="f2765-178">Benzer şekilde, **İşlevler** sağ bölmesinde seçili olan bir işlevi geçerli ifadeye yapıştırmak için **İşlev ekle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2765-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="f2765-179">ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı yapılandırılan ifadenin hep sonuna yapıştırılır.</span><span class="sxs-lookup"><span data-stu-id="f2765-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="f2765-180">Gelişmiş ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı, yapılandırılan ifadenin herhangi bir yerine yapıştırılır.</span><span class="sxs-lookup"><span data-stu-id="f2765-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="f2765-181">Verileri yapıştırmak istediğiniz yeri belirtmek için imleci kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f2765-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="f2765-182">[![ER formül düzenleyicisi](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="f2765-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="f2765-183"><a name="SyntaxColorization">Sözdizimi renklendirme</a></span><span class="sxs-lookup"><span data-stu-id="f2765-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="f2765-184">Şu anda, ifadelerin aşağıdaki kısımlarını vurgulamak için farklı renkler kullanılıyor:</span><span class="sxs-lookup"><span data-stu-id="f2765-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="f2765-185">Bir metin sabitinin etiket kodunu temsil edebilen, ayraç içindeki metin.</span><span class="sxs-lookup"><span data-stu-id="f2765-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="f2765-186">[![ER formül düzenleyicisi](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="f2765-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="f2765-187">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="f2765-187">Limitations</span></span>

<span data-ttu-id="f2765-188">Düzenleyici şu anda aşağıdaki web tarayıcılarında desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="f2765-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="f2765-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="f2765-189">Chrome</span></span>
- <span data-ttu-id="f2765-190">Edge</span><span class="sxs-lookup"><span data-stu-id="f2765-190">Edge</span></span>
- <span data-ttu-id="f2765-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="f2765-191">Firefox</span></span>
- <span data-ttu-id="f2765-192">Opera</span><span class="sxs-lookup"><span data-stu-id="f2765-192">Opera</span></span>
- <span data-ttu-id="f2765-193">Safari</span><span class="sxs-lookup"><span data-stu-id="f2765-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2765-194">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f2765-194">Additional resources</span></span>

- [<span data-ttu-id="f2765-195">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="f2765-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f2765-196">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="f2765-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="f2765-197">Monaco editor</span><span class="sxs-lookup"><span data-stu-id="f2765-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
