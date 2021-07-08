---
title: Elektronik raporlama gelişmiş formül düzenleyicisi
description: Bu konu, Elektronik raporlama (ER) model eşlemesi ve biçim bileşenlerinde ifade yapılandırmak için, gelişmiş formül düzenleyicinin nasıl kullanılabileceğini açıklamaktadır.
author: NickSelin
ms.date: 06/17/2021
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
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270719"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="9c9aa-103">Elektronik raporlama gelişmiş formül düzenleyicisi</span><span class="sxs-lookup"><span data-stu-id="9c9aa-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c9aa-104">[Elektronik raporlama](general-electronic-reporting.md) [formül düzenleyicisine](general-electronic-reporting-formula-designer.md) ek olarak, Elektronik raporlama (ER) ifadelerini yapılandırma deneyimini geliştirmek için gelişmiş Elektronik raporlama formül düzenleyicisini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="9c9aa-105">Gelişmiş düzenleyici, [Monaco editor](https://microsoft.github.io/monaco-editor) tarafından sunulan, tarayıcı tabanlı ve güçlü bir düzenleyicidir.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="9c9aa-106">En sık kullanılan gelişmiş düzenleyici özellikleri bu konuda açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="9c9aa-107">Kodu otomatik biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="9c9aa-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="9c9aa-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="9c9aa-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="9c9aa-109">Kod tamamlama</span><span class="sxs-lookup"><span data-stu-id="9c9aa-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="9c9aa-110">Kod gezintisi</span><span class="sxs-lookup"><span data-stu-id="9c9aa-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="9c9aa-111">Kod yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9c9aa-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="9c9aa-112">Bul ve değiştir</span><span class="sxs-lookup"><span data-stu-id="9c9aa-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="9c9aa-113">Veri yapıştırma</span><span class="sxs-lookup"><span data-stu-id="9c9aa-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="9c9aa-114">Sözdizimi renklendirme</span><span class="sxs-lookup"><span data-stu-id="9c9aa-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="9c9aa-115"><a name="ActivateAdvEditor">Gelişmiş formül düzenleyicisini etkinleştirme</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="9c9aa-116">Microsoft Dynamics 365 Finance kurulumunuzda gelişmiş formül düzenleyicisini kullanmaya başlamak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="9c9aa-117">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="9c9aa-118">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="9c9aa-119">**Kullanıcı parametreleri** iletişim kutusunun **Yürütme izleme** bölümünde **Gelişmiş formül düzenleyicisini etkinleştir** parametresini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="9c9aa-120">[![Kullanıcı parametreleri iletişim kutusu, Gelişmiş formül düzenleyiciyi etkinleştir parametresi vurgulanmış olarak](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9c9aa-121">Bu parametrenin kullanıcıya özel ve şirkete özel olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="9c9aa-122">Microsoft Dynamics 365 Finance sürüm 10.0.19'u kullanmaya başlayarak hangi ER formül düzenleyicisinin varsayılan olarak sunulacağını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="9c9aa-123">Geçerli Finance kurulumunun tüm kullanıcıları ve şirketleri için Gelişmiş Formül Düzenleyicisini etkinleştirmek üzere aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="9c9aa-124">**Özellik yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="9c9aa-125">Listede **ER gelişmiş formül düzenleyicisini tüm kullanıcılar için varsayılan olarak ayarla** özelliğini bulup seçin ve ardından **Şimdi etkinleştir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="9c9aa-126">**Kuruluş yönetimi**  > **Elektronik raporlama** > **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="9c9aa-127">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="9c9aa-128">**Kullanıcı parametreleri** iletişim kutusunda, **Gelişmiş formül düzenleyicisini devre dışı bırak** parametresini bulun ve **Hayır** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="9c9aa-129">[![Kullanıcı parametreleri iletişim kutusu, Gelişmiş formül düzenleyiciyi devre dışı bırak parametresi vurgulanmış olarak](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9c9aa-130">**Gelişmiş Formül Düzenleyicisini etkinleştir** ve **Gelişmiş Formül Düzenleyicisini devre dışı bırak** parametrelerinin değerleri her kullanıcı için ayrı tutulur ve **ER gelişmiş formül düzenleyicisini tüm kullanıcılar için varsayılan olarak ayarla** özelliğinin durumuna bağlı olarak **Kullanıcı parametreleri** iletişim kutusunda sunulur.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-131"><a name="Autoformatting">Kodu otomatik biçimlendirme</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="9c9aa-132">Birden fazla kod satırı içeren karmaşık bir ifade yazdığınız zaman, yeni bir girilen satırın girintilemesi önceki satırın girintilemesine göre otomatik olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="9c9aa-133">Satırları seçip girintilemelerini **Sekme**'ye veya **Üst Krkt+Sekme** tuşlarına basarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="9c9aa-134">[![Satırları seçme ve girintiyi değiştirmeyi gösteren ER formül düzenleyicisi GIF dosyası](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="9c9aa-135">Otomatik biçimlendirme, bakımı ve yapılandırılan mantığın anlaşılmasını kolaylaştırmak için tüm ifadeyi iyi biçimlendirilmiş durumda tutmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="9c9aa-137">Düzenleyici, ifadeyi daha hızlı yazmanıza ve yazım hatalarını önlemenize yardımcı olmak için sözcük tamamlama sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="9c9aa-138">Yeni metin eklemeye başladığınızda, düzenleyici, girdiğiniz karakterleri içeren ER işlevlerinde desteklenen işlevlerin bir listesini otomatik olarak sunar.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="9c9aa-139">Yapılandırılmış bir ifadenin herhangi bir yerinde **Ctrl + Boşluk** tuşlarına basarak IntelliSense'i de tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="9c9aa-140">[![IntelliSense tetiklemeyi gösteren ER formül düzenleyici GIF dosyası](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-141"><a name="CodeCompletion">Kod tamamlama</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="9c9aa-142">Düzenleyici aşağıdaki eylemlerle kodun otomatik olarak tamamlanmasını sağlar:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="9c9aa-143">Açma ayracı girilince bir kapatma ayracı girip, imleci ayraçların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="9c9aa-144">İlk tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="9c9aa-145">İlk çift tırnak girilince ikincisini ekleyip, imleci tırnakların içinde tutarak.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="9c9aa-146">[![Kod tamamlamayı otomatik olarak sağlayan düzenleyiciyi gösteren ER formül düzenleyici GIF dosyası](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="9c9aa-147">Yazılan ayracın üzerine geldiğinizde, bu çiftin ikinci ayracı, destekledikleri yapıyı gösterecek şekilde otomatik olarak vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-148"><a name="CodeNavigation">Kod gezintisi</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="9c9aa-149">Komut paletini veya bağlam menüsünü kullanıp **Go to** komutunu yazarak ifadenizde gerekli sembolleri veya çizgileri bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="9c9aa-150">Örneğin, **8**. satıra atlamak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="9c9aa-151">**Ctrl + G** tuşlarına basın, **8** değerini girin ve **Enter** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="9c9aa-152">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-152">-or-</span></span>

- <span data-ttu-id="9c9aa-153">**F1** tuşuna basın, **G** yazın, **Go to line**'ı seçin, **8** değerini girin ve **Enter** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="9c9aa-154">[![Komut paletini kullanarak bir ifadenin bölümlerinin nasıl bulunacağını gösteren ER formül düzenleyici GIF dosyası](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-155"><a name="CodeStructuring">Kod yapılandırma</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="9c9aa-156">[IF](er-functions-logical-if.md) veya [CASE](er-functions-logical-case.md) gibi bazı işlevlerin kodu otomatik olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="9c9aa-157">Yalnızca ilgilenmeniz gereken kod parçasına odaklanmak için, bir ifadenin düzenlenebilen kısmını küçültmek üzere bu kodun katlama bölgelerini genişletebilir veya daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="9c9aa-158">Bunun için katla/aç geçişi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="9c9aa-159">Örneğin tüm bölgeleri katlamak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="9c9aa-160">**Ctrl+K** tuşlarına basın</span><span class="sxs-lookup"><span data-stu-id="9c9aa-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="9c9aa-161">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-161">-or-</span></span>

- <span data-ttu-id="9c9aa-162">**F1**'e basın, **FO**'ya basın, **Tümünü katla**'yı seçin ve **Enter**'a basın</span><span class="sxs-lookup"><span data-stu-id="9c9aa-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="9c9aa-163">Tüm bölgeleri açmak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="9c9aa-164">**Ctrl+J** tuşlarına basın</span><span class="sxs-lookup"><span data-stu-id="9c9aa-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="9c9aa-165">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-165">-or-</span></span>
  
- <span data-ttu-id="9c9aa-166">**F1**'e basın, **UN** yazın, **Tümünü aç**'ı seçin ve **Enter**'a basın</span><span class="sxs-lookup"><span data-stu-id="9c9aa-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="9c9aa-167">[![Kodu açmayı gösteren ER formül düzenleyici GIF dosyası](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-168"><a name="FindAndReplace">Bul ve değiştir</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="9c9aa-169">Belirli bir metnin yinelemelerini bulmak için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="9c9aa-170">Seçili metnin bir sonraki yinelemesini bulmak için **Ctrl + F** ve ardından **F3** tuşlarına basın veya önceki yinelemeyi bulmak için **Shift + F3** tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="9c9aa-171">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-171">-or-</span></span>
  
- <span data-ttu-id="9c9aa-172">**F1** tuşuna basın, **F** yazın ve seçili metni bulmak için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="9c9aa-173">Belirli bir metnin yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="9c9aa-174">**Ctrl+H** tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="9c9aa-175">Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="9c9aa-176">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-176">-or-</span></span>
  
- <span data-ttu-id="9c9aa-177">**F1** tuşuna basın, **R** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="9c9aa-178">Alternatif metni girip, geçerli ifadede seçili metni veya bu metnin yinelemelerini değiştirmek için Değiştir seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="9c9aa-179">Belirli bir metnin tüm yinelemelerini değiştirmek için, ifadenizde metni seçin ve aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="9c9aa-180">**Ctrl + F2** tuşlarına basın ve ardından alternatif metni girin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="9c9aa-181">-veya-</span><span class="sxs-lookup"><span data-stu-id="9c9aa-181">-or-</span></span>
  
- <span data-ttu-id="9c9aa-182">**F1** tuşuna basın, **C** yazın ve seçili metni değiştirmek için gerekli seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="9c9aa-183">Alternatif metni girin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-183">Enter the alternative text.</span></span>

<span data-ttu-id="9c9aa-184">[![Bul ve değiştiri gösteren ER formül düzenleyici GIF dosyası](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-185"><a name="DataPasting">Veri kaynaklarını ve işlevleri yapıştırma</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="9c9aa-186">**Veri kaynağı** sol bölmesinde seçili olan bir veri kaynağını geçerli ifadeye yapıştırmak için **Veri kaynağı ekle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="9c9aa-187">Benzer şekilde, **İşlevler** sağ bölmesinde seçili olan bir işlevi geçerli ifadeye yapıştırmak için **İşlev ekle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="9c9aa-188">ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı yapılandırılan ifadenin hep sonuna yapıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="9c9aa-189">Gelişmiş ER formül düzenleyicisi kullanıyorsanız, seçilen bir işlev veya seçilen bir veri kaynağı, yapılandırılan ifadenin herhangi bir yerine yapıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="9c9aa-190">Verileri yapıştırmak istediğiniz yeri belirtmek için imleci kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="9c9aa-191">[![Veri kaynağı eklemeyi ve bir işlevi yapıştırmayı gösteren ER formül düzenleyicisi GIF dosyası](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="9c9aa-192"><a name="SyntaxColorization">Sözdizimi renklendirme</a></span><span class="sxs-lookup"><span data-stu-id="9c9aa-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="9c9aa-193">Şu anda, ifadelerin aşağıdaki kısımlarını vurgulamak için farklı renkler kullanılıyor:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="9c9aa-194">Bir metin sabitinin etiket kodunu temsil edebilen, ayraç içindeki metin.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="9c9aa-195">[![ER formül düzenleyicisi](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="9c9aa-196">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="9c9aa-196">Limitations</span></span>

<span data-ttu-id="9c9aa-197">Düzenleyici şu anda aşağıdaki web tarayıcılarında desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="9c9aa-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="9c9aa-198">Chrome</span></span>
- <span data-ttu-id="9c9aa-199">Edge</span><span class="sxs-lookup"><span data-stu-id="9c9aa-199">Edge</span></span>
- <span data-ttu-id="9c9aa-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="9c9aa-200">Firefox</span></span>
- <span data-ttu-id="9c9aa-201">Opera</span><span class="sxs-lookup"><span data-stu-id="9c9aa-201">Opera</span></span>
- <span data-ttu-id="9c9aa-202">Safari</span><span class="sxs-lookup"><span data-stu-id="9c9aa-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c9aa-203">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9c9aa-203">Additional resources</span></span>

- [<span data-ttu-id="9c9aa-204">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="9c9aa-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9c9aa-205">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="9c9aa-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="9c9aa-206">Monaco editor</span><span class="sxs-lookup"><span data-stu-id="9c9aa-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
