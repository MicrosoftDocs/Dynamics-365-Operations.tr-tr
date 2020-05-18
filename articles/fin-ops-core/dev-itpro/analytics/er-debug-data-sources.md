---
title: Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama
description: Bu konu, yapılandırılmış veri akışını ve dönüştürmeyi daha iyi anlamak için yürütülen bir ER biçiminin veri kaynaklarında nasıl hata ayıklayabileceğinizi açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318678"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="4a1f5-103">Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="4a1f5-104">Giden belgeler oluşturmak için bir Elektronik raporlama (ER) çözümü [yapılandırdığınızda](tasks/er-format-configuration-2016-11.md) uygulamadan veri almak ve oluşturulan çıktıya bu verileri girmek için kullanılan yöntemleri belirlersiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="4a1f5-105">ER çözümünün yaşam döngüsü desteğini daha etkili hale getirmek için, bir ER [veri modeli](general-electronic-reporting.md#DataModelComponent) ve onun [eşlemesini](general-electronic-reporting.md#ModelMappingComponent) ve ayrıca bir ER [biçimi ](general-electronic-reporting.md#FormatComponentOutbound) ve onun eşleme bileşenlerini oluşturmanız gerekir; böylece model eşleme uygulamaya özel olacak ve diğer bileşenler uygulama belirsiz olarak kalacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="4a1f5-106">Bu nedenle, birkaç ER bileşeni oluşturulan çıktıya veri girme işlemini [etkileyebilir](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="4a1f5-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="4a1f5-107">Bazı durumlarda, oluşturulan çıktının verileri uygulama veritabanındaki aynı verilerden farklı görünür.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="4a1f5-108">Bu durumlarda, veri dönüştürme için hangi ER bileşeninin sorumlu olduğunu belirlemek istersiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="4a1f5-109">ER veri kaynağı hata ayıklama özelliği, bu araştırmaya harcanan zamanı ve maliyeti önemli ölçüde azaltır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="4a1f5-110">Bir ER biçimi yürütmesini kesebilir ve veri kaynağı hata ayıklama arabirimini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="4a1f5-111">Arabirimde, kullanılabilir veri kaynaklarına göz atabilir ve yürütme için tek bir veri kaynağı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="4a1f5-112">Bu el ile yürütme, bir ER biçiminin gerçek çalışması sırasındaki veri kaynağı yürütmesinin benzetimi yapar.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="4a1f5-113">Sonuç, alınan verileri analiz edebileceğiniz bir sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="4a1f5-114">Veri kaynağı hata ayıklama özelliğini etkinleştirmek için, **Biçim çalıştırmada veri hata ayıklamasını etkinleştir** seçeneğini ER kullanıcı parametrelerinde **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="4a1f5-115">Böylece, giden belgeler oluşturmak üzere bir ER biçimi çalıştırırken veri kaynağı hata ayıklaması başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="4a1f5-116">Ayrıca, [ER İşlem tasarımcısında](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) yapılandırılan bir ER biçimi için veri kaynağı hata ayıklamasını başlatmak için **Hata ayıklamayı başlat** seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="4a1f5-117">Bu konu, yürütülen ER biçimlerinde veri kaynağı hata ayıklamasını başlatmak için yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="4a1f5-118">Veri akışını ve veri dönüştürme işlemlerini anlamanıza yardımcı olabilecek bilgiler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="4a1f5-119">Bu konudaki örnekler, satıcı ödemelerini işlemede kullanılan iş sürecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="4a1f5-120">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="4a1f5-120">Limitations</span></span>

<span data-ttu-id="4a1f5-121">Veri kaynağı hata ayıklayıcı, giden belgeler oluşturmak üzere çalıştırılan ER biçimlerinde kullanılan veri kaynaklarının verilerine erişmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="4a1f5-122">Gelen belgeleri ayrıştırmak üzere tasarlanan ER biçimlerinin veri kaynaklarında hata ayıklamak için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="4a1f5-123">Aşağıdaki ER biçimi ayarlarına şu anda veri kaynağı hata ayıklama için erişilemez:</span><span class="sxs-lookup"><span data-stu-id="4a1f5-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="4a1f5-124">Biçim dönüşümleri</span><span class="sxs-lookup"><span data-stu-id="4a1f5-124">Format transformations</span></span>
- <span data-ttu-id="4a1f5-125">Biçim ve eşleme doğrulama kuralları</span><span class="sxs-lookup"><span data-stu-id="4a1f5-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="4a1f5-126">İfadeleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-126">Enabling expressions</span></span>
- <span data-ttu-id="4a1f5-127">Bellek içi veri toplama ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4a1f5-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4a1f5-128">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="4a1f5-128">Prerequisites</span></span>

- <span data-ttu-id="4a1f5-129">Bu konudaki örnekleri tamamlamak için aşağıdaki [rollerden](../sysadmin/tasks/assign-users-security-roles.md) birine erişiminiz olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="4a1f5-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="4a1f5-130">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="4a1f5-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="4a1f5-131">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="4a1f5-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4a1f5-132">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="4a1f5-132">System administrator</span></span>

- <span data-ttu-id="4a1f5-133">Şirketin **DEMF** olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="4a1f5-134">Bu konunun [Ek 1](#appendix1) bölümündeki adımları izleyerek satıcı ödemelerini işlemek için gerekli olan Microsoft ER çözümü bileşenlerini indirin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="4a1f5-135">İndireceğiniz ER çözümünü kullanarak satıcı ödemesi işleme için Borç hesaplarını hazırlamak üzere bu konunun [Ek 2](#appendix2) bölümündeki konuları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="4a1f5-136">Ödeme dosyasını almak için satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="4a1f5-137">Satıcı ödemelerini işlemek için bu konudaki [Ek 3](#appendix3) bölümünde yer alan adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Satıcı ödeme işlemi devam ediyor](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="4a1f5-139">Zip dosyasını indirin ve yerel bilgisayarınıza kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="4a1f5-140">**ISO20022 Credit transfer.xml** ödeme dosyasını zip dosyasından çıkarın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="4a1f5-141">XML dosya görüntüleyicisini kullanarak çıkarılan ödeme dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="4a1f5-142">Ödeme dosyasında, satıcı banka hesabının Uluslararası Banka Hesabı Numarası (IBAN) kodu boşluk içermez.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="4a1f5-143">Bu nedenle, **Banka hesapları** sayfasına [girilmiş](#enteredIBANcode) olan değerden farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![Boşluk içermeyen IBAN kodu](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="4a1f5-145">ER veri kaynağı hata ayıklayıcısını, IBAN kodundaki boşlukları kırpmak için ER çözümünün hangi bileşeninin kullanıldığını öğrenmek üzere kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="4a1f5-146">Veri kaynağı hata ayıklamayı açma</span><span class="sxs-lookup"><span data-stu-id="4a1f5-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="4a1f5-147">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4a1f5-148">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="4a1f5-149">**Biçim çalıştırma sırasında veri hatası ayıklamayı etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4a1f5-150">Bu parametre kullanıcıya özel ve şirkete özeldir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-150">This parameter is user-specific and company-specific.</span></span>

    ![Kullanıcı parametreleri iletişim kutusu](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="4a1f5-152">Hata ayıklama için satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="4a1f5-153">Satıcı ödemelerini işlemek için bu konudaki [Ek 3](#appendix3) bölümünde yer alan adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="4a1f5-154">İleti kutusunda, satıcı ödeme işlemini kesintiye uğratmak istediğinizi doğrulamak için **Evet**'i seçin ve bunun yerine **Veri Kaynaklarında Hata Ayıkla** sayfasında veri kaynağı hata ayıklama işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Onay iletisi kutusu](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="4a1f5-156">Ödeme işlemede kullanılan veri kaynaklarında hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="4a1f5-157">Model eşlemesinde hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-157">Debug the model mapping</span></span>

1. <span data-ttu-id="4a1f5-158">**Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşinden başlatmak için **Model eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="4a1f5-159">Soldaki veri kaynağı bölmesinde, **\$notSentTransactions** veri kaynağını seçin ve **Tüm kayıtları oku**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="4a1f5-160">Seçilen veri kaynağından okunacak uygun kayıt sayısını zorlamak için **1 kayıt oku**, **10 kayıt oku**, **100 kayıt oku** veya **Tüm kayıtları oku** seçeneğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="4a1f5-161">Bu şekilde, çalışan ER biçiminden veri kaynağına erişim benzetimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="4a1f5-162">Sağdaki veri bölmesinde **Tümünü genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="4a1f5-163">**Kayıt listesi** türündeki seçili kaynağın tek bir kayıt içerdiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="4a1f5-164">**\$notSentTransactions** veri kaynağını genişletin ve iç içe geçmiş **vendBankAccountInTransactionCompany()** yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="4a1f5-165">**vendBankAccountInTransactionCompany()** yöntemini genişletin ve iç içe geçmiş **IBAN** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="4a1f5-166">**Değeri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-166">Select **Get value**.</span></span>

    <span data-ttu-id="4a1f5-167">Seçili veri kaynağının seçili alanının değerini okunacak şekilde zorlamak için **Değeri al**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="4a1f5-168">Bu şekilde, çalışan ER biçiminden bu alana erişim benzetimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="4a1f5-169">**Tümünü genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-169">Select **Expand all**.</span></span>

    ![Model eşlemedeki IBAN alanının değeri](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="4a1f5-171">Gördüğünüz gibi, satıcı banka hesabı için döndürdüğü IBAN kodu boşluklar içerdiğinden model eşleme kesilen boşluklardan sorumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4a1f5-172">Bu nedenle, veri kaynağı hata ayıklamasını sürdürmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="4a1f5-173">Biçim eşlemede hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-173">Debug the format mapping</span></span>

1. <span data-ttu-id="4a1f5-174">**Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşininden sürdürmek için **Biçim eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="4a1f5-175">**\$PaymentByDebtor** veri kaynağını seçin ve ardından **Tüm kayıtları oku**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="4a1f5-176">**\$PaymentByDebtor** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="4a1f5-177">**\$PaymentByDebtor.Lines** öğesini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="4a1f5-178">**\$PaymentByDebtor.Lines.CreditorAccount** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="4a1f5-179">**\$PaymentByDebtor.Lines.CreditorAccount.Identification** öğesini genişletin ve **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="4a1f5-180">**Değeri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-180">Select **Get value**.</span></span>
8. <span data-ttu-id="4a1f5-181">**Tümünü genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-181">Select **Expand all**.</span></span>

    ![Biçim eşlemedeki IBAN alanının değeri](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="4a1f5-183">Gördüğünüz gibi, satıcı banka hesabı için döndürdükleri IBAN kodu boşluklar içerdiğinden biçim eşlemenin veri kaynakları kesilen boşluklardan sorumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4a1f5-184">Bu nedenle, veri kaynağı hata ayıklamasını sürdürmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="4a1f5-185">Biçimde hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-185">Debug the format</span></span>

1. <span data-ttu-id="4a1f5-186">**Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşininden sürdürmek için **Biçim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="4a1f5-187">**ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** öğesini seçmek için biçim öğelerini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="4a1f5-188">**ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** öğesini seçmek için biçim öğelerini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="4a1f5-189">**ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** öğesini seçmek için biçim öğelerini genişletin ve ardından **Değeri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="4a1f5-190">**Tümünü genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-190">Select **Expand all**.</span></span>

    ![Biçimdeki IBAN alanının değeri](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="4a1f5-192">Gördüğünüz gibi, satıcı banka hesabı için döndürdüğü IBAN kodu boşluklar içerdiğinden biçim bağlaması kesilen boşluklardan sorumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4a1f5-193">Bu nedenle, **BankIBAN** öğesi, boşlukları kesen bir biçim dönüşümü kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="4a1f5-194">Veri kaynağı hata ayıklayıcısını kapatın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="4a1f5-195">Biçim dönüştürmelerini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-195">Review the format transformations</span></span>

1. <span data-ttu-id="4a1f5-196">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4a1f5-197">**Yapılandırmalar** sayfasında, **Ödeme modeli** \> **ISO20022 Alacak transferi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4a1f5-198">**Tasarımcı**'yı seçin ve ardından **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**'ı seçmek için öğeleri genişletin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![Biçim tasarımcısı sayfasındaki BankIBAN öğesi](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="4a1f5-200">Gördüğünüz gibi, **BankIBAN** öğesi **alfasayısal olmayanı kaldır** dönüşümünü kaldırmak için yapılandırılmışır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="4a1f5-201">**Dönüştürmeler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN öğesi için dönüştürmeler sekmesi](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="4a1f5-203">Gördüğünüz gibi, **alfasayısal olmayanı kaldır** dönüştürme işlemi, sağlanan metin dizesinden boşlukları kesen bir ifade kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="4a1f5-204">İşlem tasarımcısında hata ayıklamaya başlatma</span><span class="sxs-lookup"><span data-stu-id="4a1f5-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="4a1f5-205">Doğrudan İşlem tasarımcısından çalıştırılabilen ER biçiminin taslak sürümünü yapılandırdığınızda, Eylem Bölmesinde **Hata Ayıklamayı Başlat**'ı seçerek veri kaynağı hata ayıklayıcıya erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Biçim tasarımcısı sayfasındaki Hata Ayıklamayı Başlat düğmesi](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="4a1f5-207">Düzenlenen ER biçiminin biçim eşlemesi ve biçim bileşenleri hata ayıklama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="4a1f5-208">Model eşleme tasarımcısında hata ayıklamaya başlatma</span><span class="sxs-lookup"><span data-stu-id="4a1f5-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="4a1f5-209">**Model eşleme** sayfasından çalıştırılabilen bir ER model eşlemesi yapılandırdığınızda, Eylem Bölmesinde **Hata Ayıklamayı Başlat**'ı seçerek veri kaynağı hata ayıklayıcıya erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Model eşleme tasarımcısı sayfasındaki Hata Ayıklamayı Başlat düğmesi](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="4a1f5-211">Düzenlenmekte olan ER eşlemesinin model eşleme bileşeni hata ayıklama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="4a1f5-212">Ek 1: ER çözümü alma</span><span class="sxs-lookup"><span data-stu-id="4a1f5-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="4a1f5-213">ER çözümü indirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-213">Download an ER solution</span></span>

<span data-ttu-id="4a1f5-214">İşlenen bir satıcı ödemesi için elektronik ödeme dosyası oluşturmak üzere bir ER çözümü kullanmak istiyorsanız, Microsoft Dynamics LifeCycle Services'taki (LCS) Paylaşılan varlık kitaplığından veya Genel depodan **ISO20022 Alacak transferi** ER ödeme biçimini [indirebilirsiniz](download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="4a1f5-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Yapılandırma deposu sayfasındaki ER ödeme biçimini içe aktarma](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="4a1f5-216">Seçili ER biçimine ek olarak, aşağıdaki [yapılandırmalar](general-electronic-reporting.md#Configuration) Microsoft Dynamics 365 Finance kurulumunuza **ISO20022 Alacak transferi** ER çözümünüzün bir parçası olarak otomatik olarak aktarılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="4a1f5-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="4a1f5-217">**Ödeme modeli** [ER veri modeli yapılandırması](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="4a1f5-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="4a1f5-218">**ISO20022 Alacak transferi** [ER biçimi yapılandırması](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="4a1f5-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="4a1f5-219">**Ödeme modeli eşleme 1611** [ER modeli eşleme yapılandırması](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="4a1f5-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="4a1f5-220">**ISO20022 hedefine ödeme modeli eşleme** ER modeli eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="4a1f5-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="4a1f5-221">Bu yapılandırmaları ER çerçevesinin **Yapılandırmalar** sayfasında bulabilirsiniz (**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**).</span><span class="sxs-lookup"><span data-stu-id="4a1f5-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Yapılandırmalar sayfasında içe aktarılan yapılandırmalar](./media/er-data-debugger-configurations.png)

<span data-ttu-id="4a1f5-223">Daha önce listelenmiş yapılandırmalardan herhangi bir yapılandırma ağacında eksikse, bunları **ISO20022 Alacak transferi** ER ödeme biçimini indirdiğiniz şekilde LCS paylaşılan varlık kitaplığından el ile indirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="4a1f5-224">İndirilen ER çözümünü analiz etme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="4a1f5-225">Model eşlemeyi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-225">Review the model mapping</span></span>

1. <span data-ttu-id="4a1f5-226">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4a1f5-227">**Ödeme modeli** \> **Ödeme modeli eşlemesi 1611**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="4a1f5-228">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-228">Select **Designer**.</span></span>
4. <span data-ttu-id="4a1f5-229">**Ödeme modeli eşlemesi ISO20022 CT** eşleme kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="4a1f5-230">**Tasarımcı**'yı seçin ve sonra açılan model eşlemeyi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="4a1f5-231">Veri modelinin **Ödemeler** alanının, işlenmekte olan satıcı ödemesi satırlarını döndüren **\$notSentTransactions** veri kaynağına bağlı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Model eşleme tasarımcısı sayfasındaki ödemeler alanı](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="4a1f5-233">Biçim eşlemeyi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-233">Review the format mapping</span></span>

1. <span data-ttu-id="4a1f5-234">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4a1f5-235">**Ödeme modeli** \> **ISO20022 Alacak transferi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4a1f5-236">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-236">Select **Designer**.</span></span>
4. <span data-ttu-id="4a1f5-237">**Eşleme** sekmesinde, açılan biçim eşlemesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="4a1f5-238">**ISO20022CTReports** \> **XMLHeader** dosyasının **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** öğesinin veri modelinin **Ödemeler** alanındaki kayıtları gruplandırılan **\$PaymentByDebtor** veri kaynağına bağlı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![Biçim tasarımcısı sayfasındaki PmtInf öğesi](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="4a1f5-240">Biçimi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-240">Review the format</span></span>

1. <span data-ttu-id="4a1f5-241">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4a1f5-242">**Ödeme modeli** \> **ISO20022 Alacak transferi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4a1f5-243">**Tasarımcı**'yı seçin ve sonra açılan biçimi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="4a1f5-244">**Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** altındaki biçimin ödeme dosyasındaki satıcı hesabının IBAN kodunu girmek üzere yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![Biçim tasarımcısı sayfasındaki BankIBAN öğesi](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="4a1f5-246">Ek 2: Borç hesaplarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4a1f5-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="4a1f5-247">Satıcı özelliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-247">Modify a vendor property</span></span>

1. <span data-ttu-id="4a1f5-248">**Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="4a1f5-249">**DE-01002** satıcısını seçin ve ardından Eylem Bölmesinde, **Satıcı** sekmesinde **Ayar** grubunda, **Banka hesapları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="4a1f5-250">**Kimlik** hızlı sekmesinde, **IBAN** alanına <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55** girin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="4a1f5-251">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-251">Select **Save**.</span></span>

![Satıcı banka hesapları sayfasında ayarlanan IBAN alanı](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="4a1f5-253">Ödeme yöntemi ayarlama</span><span class="sxs-lookup"><span data-stu-id="4a1f5-253">Set up a method of payment</span></span>

1. <span data-ttu-id="4a1f5-254">**Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="4a1f5-255">**SEPA CT** ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="4a1f5-256">**Dosya biçimleri** Hızlı sekmesinde **Dosya biçimlerşi** bölümünde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="4a1f5-257">**Dışa aktarma biçimi yapılandırması** alanında, **ISO20022 Alacak transferi** ER biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="4a1f5-258">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-258">Select **Save**.</span></span>

![Ödeme yöntemleri sayfasındaki dosya biçimi ayarları](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="4a1f5-260">Satıcı ödemesi ekleme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-260">Add a vendor payment</span></span>

1. <span data-ttu-id="4a1f5-261">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="4a1f5-262">Yeni bir ödeme günlüğü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="4a1f5-263">**Satırlar**'ı seçin ve yeni bir ödeme satırı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="4a1f5-264">**Hesap** alanında satıcı **DE-01002**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="4a1f5-265">**Borç** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="4a1f5-266">**Ödeme yöntemi** alanında **SEPA CT**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="4a1f5-267">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-267">Select **Save**.</span></span>

![Satıcı ödemeleri sayfasına eklenen satıcı ödemesi](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="4a1f5-269">Ek 3: Satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="4a1f5-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="4a1f5-270">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="4a1f5-271">**Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü ve ardından **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="4a1f5-272">Ödeme satırını seçin ve **Ödeme durumu** \> **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="4a1f5-273">**Ödemeleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="4a1f5-274">**Ödeme yöntemi** alanında **SEPA CT**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="4a1f5-275">**Banka hesabı** alanında **DEMF OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="4a1f5-276">**Ödeme oluştur** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="4a1f5-277">**Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4a1f5-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
