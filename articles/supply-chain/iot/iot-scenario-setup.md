---
title: IoT Zekası için senaryo kurulumu
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management uygulamasında IoT Zekası için senaryoların nasıl yapılandırılacağını açıklamaktadır.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005264"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="85d1d-103">IoT Zekası için senaryo kurulumu</span><span class="sxs-lookup"><span data-stu-id="85d1d-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85d1d-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management uygulamasında IoT Zekası için senaryoların nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85d1d-105">Senaryoları ayarlamadan önce, [Microsoft Dynamics Lifecycle Services (LCS) ayarlamanız](iot-lcs-setup.md) gerekir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="85d1d-106">Bu konuda, **Ekipman kesinti süresi** senaryosunu bir makine arızalandığında Supply Chain Management'ta bildirim oluşturulacak şekilde yapılandıracaksınız.</span><span class="sxs-lookup"><span data-stu-id="85d1d-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="85d1d-107">Bu konu ayrıca, bir maddenin özniteliği belirli bir aralığın dışında olduğunda bir bildirimin oluşturulması için **Ürün kalite** senaryosunun nasıl yapılandırılacağını ve üretim verimi bir eşik değerinin altına düştüğünde bir bildirim üretilmesi için **Üretim gecikmeleri** senaryosunun nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="85d1d-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="85d1d-108">Supply Chain Management'ta Ekipman kesinti süresi senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="85d1d-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="85d1d-109">**Ekipman kesinti süresi** senaryosu, bir **PartOut** sinyalini makine uyarı eşiğine eşler.</span><span class="sxs-lookup"><span data-stu-id="85d1d-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="85d1d-110">Makine, yalnızca senaryo için seçildiğinde ve Supply Chain Management içinde **Çalışıyor** olarak ayarlandığında izlenir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="85d1d-111">Makineden son alınan **PartOut** sinyalinden bu yana geçen süre, uyarı eşiğinden büyükse **Makine arızası** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="85d1d-112">Makine hala çalışıyorsa bir sonraki **PartOut** sinyali alındığında **Makine devrede** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="85d1d-113">Makine, 30 dakika boyunca arızada kalırsa yeni bir **Makine arızası** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="85d1d-114">**Ekipman kesinti süresi** senaryosu, aşağıdaki bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="85d1d-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="85d1d-115">Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="85d1d-116">Eşlenmiş bir makinenin **PartOut** sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir ve benzersiz bir ad eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="85d1d-117">Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, Azure IoT Hub iletisinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="85d1d-118">Senaryoyu yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="85d1d-119">Supply Chain Management'ta oturun açın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="85d1d-120">IoT Zekası özellik bayrağını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="85d1d-121">Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="85d1d-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="85d1d-122">Ölçümleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-122">Configure the metrics.</span></span> <span data-ttu-id="85d1d-123">Daha fazla bilgi için bkz. [Ölçümleri yapılandıma](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="85d1d-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="85d1d-124">**Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo Yönetimi** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="85d1d-125">**Ekipman kesinti süresi** kutusunda yapılandırma sihirbazını açmak için **Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="85d1d-126">Sihirbazı ilk sayfası **Ekipman sensörü şema tanımı** sayfasıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="85d1d-127">Bu sayfada, amaç, IoT Hub iletilerindeki JavaScript nesne gösterimi (JSON) biçimiyle eşleşmesi için Supply Chain Management içerisinde şemayı ayarlamak olacaktır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="85d1d-128">Birden çok ileti şeması tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="85d1d-129">Daha fazla bilgi için bkz. [IoT Hub iletilerinde şema biçimleri](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="85d1d-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="85d1d-130">Bu örnekte ileti yükü, aşağıdaki biçimi içeren bir toplu iletileri içerir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="85d1d-131">Tabloya bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="85d1d-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="85d1d-132">**Şema adı** alanını **Kod** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="85d1d-133">**Şema yolu** alanını **/payload\[\*\]/id** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="85d1d-134">**Açıklama** alanını **İleti kodu** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="85d1d-135">Tabloya başka bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="85d1d-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="85d1d-136">**Şema adı** alanını **Zaman damgası** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="85d1d-137">**Şema yolu** alanını **/payload\[\*\]/timestamp** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="85d1d-138">**Açıklama** alanını **İleti zaman damgası** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="85d1d-139">Tabloya başka bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="85d1d-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="85d1d-140">**Şema adı** alanını **Değer** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="85d1d-141">**Şema yolu** alanını **/payload\[\*\]/value** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="85d1d-142">**Açıklama** alanını **İleti değeri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85d1d-143">İletideki tüm özellikleri tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="85d1d-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="85d1d-144">Yalnızca gereksinim duyduğunuz özellikleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-144">Define only the properties that you require.</span></span> <span data-ttu-id="85d1d-145">Önceki adımlarda, **Kök zaman damgası** için bir satır oluşturmadınız.</span><span class="sxs-lookup"><span data-stu-id="85d1d-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="85d1d-146">**Kök zaman damgası** yolu **/timestamp** olacaktır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="85d1d-147">**Ekipman sensörü şema tanımı** sayfasına gitmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="85d1d-148">**Ekipman kaynak kodu** satırında **Şema adı** alanında **Kod** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="85d1d-149">**UTC saati** satırında **Şema adı** alanında **Zaman damgası** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="85d1d-150">**Parça üretildi sinyali** satırında **Şema adı** alanında **Değer** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="85d1d-151">**Ekipman kaynağı kod yapılandırması** sayfasına gitmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="85d1d-152">IoT Hub iletide değerleri Supply Chain Management kaynaklarıyla eşlemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="85d1d-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="85d1d-153">**Sinyal Veri Değerleri** tablosunda yeni bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="85d1d-154">**Değer** alanında **IoTInt.Machine1225.PartOut** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="85d1d-155">Bu değer, IoT Hub iletisindeki JSON **id** özelliğinden gelir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="85d1d-156">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-156">Select **Save**.</span></span>
    3. <span data-ttu-id="85d1d-157">**İş Kaydı Eşleme** tablosunda **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="85d1d-158">**İş kaydı türü** alanı için varsayılan değer otomatik olarak doldurulmuştur ve değiştirmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="85d1d-159">**İş kaydı** alanında, bu sinyal değerinin gönderildiği Supply Chain Management makine kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="85d1d-160">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-160">Select **Save**.</span></span>
    6. <span data-ttu-id="85d1d-161">**Machine1226** için yeni bir iş kaydı eşlemesi eklemek için bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="85d1d-162">Birden çok sinyal veri değerini Supply Chain Management'ta tek bir kayda eşleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85d1d-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="85d1d-163">İşlemek istediğiniz makineleri seçmek için **Seçili** sütununu kullanın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="85d1d-164">Tüm sinyal değerlerini tanımlamanız ve tüm makineleri seçmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="85d1d-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="85d1d-165">**Parça üretildi sinyali yapılandırması** sayfasına gitmek için **İleri** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="85d1d-166">**Sinyal Veri Değerleri** tablosuna bir satır ekleyin ve **Değer** alanını **Doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="85d1d-167">Bu değer, IoT Hub iletisindeki JSON **value** özelliğinden gelir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="85d1d-168">Senaryonuz için gereksinim duyduğunuz kadar değer ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85d1d-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="85d1d-169">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-169">Select **Save**.</span></span>
20. <span data-ttu-id="85d1d-170">**Ekipman kesinti süresi eşiği** sayfasına gitmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="85d1d-171">Listelenen makineler, daha önce sinyal değerlerine eşlenen makinelerdir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="85d1d-172">Bu sayfada, bir makinenin arızalı olup olmadığını belirlemek için bir eşik tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="85d1d-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="85d1d-173">Örneğin eşiği **10** olarak ayarlarsanız, 10 dakika boyunca bir makineden **PartOut** sinyali gelmediğinde Supply Chain Management bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="85d1d-174">**Senaryoyu etkinleştir** sayfasına gitmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="85d1d-175">Profili etkinleştirmek için seçeneği ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="85d1d-176">**Bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-176">Select **Finish**.</span></span>

<span data-ttu-id="85d1d-177">Senaryo kurulumu artık tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="85d1d-177">The scenario setup is now completed.</span></span> <span data-ttu-id="85d1d-178">IoT Zekası, IoT Hub iletilerini otomatik olarak işlemeye başlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="85d1d-179">Supply Chain Management'ta Ürün kalitesi senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="85d1d-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="85d1d-180">Maddenin özelliği, belirtilen aralığın dışındaysa **Ürün kalitesi** senaryosu bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="85d1d-181">Örneğin, bir sensör her maddenin ağırlığını IoT Hub'a gönderir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="85d1d-182">Supply Chain Management'ta, madde çok ağır veya çok hafifse bir bildirim oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="85d1d-183">**Ürün kalitesi** senaryosu, aşağıdaki bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="85d1d-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="85d1d-184">Uyarının tetiklenebilmesi için bir üretim emrinin eşlenmiş bir makinede çalışması ve eşlenen toplu iş özniteliğe sahip bir ürün üretmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="85d1d-185">Toplu iş özniteliğini temsil eden bir sinyal IoT Hub'a gönderilmelidir ve benzersiz özellik adı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="85d1d-186">Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, IoT Hub iletisinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="85d1d-187">Supply Chain Management'ta Üretim gecikmeleri senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="85d1d-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="85d1d-188">Üretim iş çıkarma yeteneği bir eşik değerinin altına düşerse **Üretim gecikmeleri** senaryosu bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="85d1d-189">Bu senaryoda, üretilen her madde için IoT Hub'a bir **PartOut** sinyali gönderilir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="85d1d-190">Supply Chain Management içinde, sipariş gecikmesi üretim emrinin çalışmak üzere zamanlandığı zaman miktarına, üretilmesi gereken maddelerin sayısına, işin çalıştığı sürenin miktarına ve teslim alınan **PartOut** sinyallerin sayısına bağlı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="85d1d-191">İş için **PartOut** sinyallerinin sayısı beklenen eşik değerinin altına düşerse bir gecikme bildirimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="85d1d-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="85d1d-192">**Üretim gecikmeleri** senaryosu, aşağıdaki bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="85d1d-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="85d1d-193">Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="85d1d-194">Eşlenmiş bir makinenin **PartOut** sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla Azure IoT Hub'a gönderilmelidir ve benzersiz bir ad eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="85d1d-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="85d1d-195">Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, IoT Hub iletisinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d1d-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="85d1d-196">Senaryoyu devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="85d1d-196">Disable a scenario</span></span>

<span data-ttu-id="85d1d-197">Senaryoyu devre dışı bırakmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="85d1d-198">Supply Chain Management'ta **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="85d1d-199">Senaryonun kutusundan **Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="85d1d-200">Son sihirbaz sayfasına gitmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85d1d-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="85d1d-201">Profili devre dışı bırakmak için seçeneği ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85d1d-201">Set the option to disable the scenario.</span></span>
