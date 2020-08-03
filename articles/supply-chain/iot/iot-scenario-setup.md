---
title: IoT Zekası için senaryo kurulumu
description: Bu konuda, IoT Zekası için Supply Chain Management'ta bir senaryonun nasıl yapılandırılacağı açıklanmaktadır.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597180"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="7346f-103">IoT Zekası için senaryo kurulumu</span><span class="sxs-lookup"><span data-stu-id="7346f-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7346f-104">Bu konuda, IoT Zekası için Supply Chain Management'ta bir senaryonun nasıl yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7346f-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="7346f-105">Senaryoları ayarlamadan önce [LCS'yi kurmalısınız](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7346f-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="7346f-106">Bu konuda, **Ekipman kesinti süresi** senaryosunu bir makine arızalandığında Supply Chain Management'ta bildirim oluşturacak şekilde yapılandıracaksınız.</span><span class="sxs-lookup"><span data-stu-id="7346f-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="7346f-107">Supply Chain Management'ta **Ekipman kesinti süresi** senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7346f-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="7346f-108">**Ekipman kesinti süresi** senaryosu, bir parça çıkış sinyalini makine uyarı eşiğine eşler.</span><span class="sxs-lookup"><span data-stu-id="7346f-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="7346f-109">Makine, yalnızca senaryo için seçildiğinde ve Supply Chain Management içinde çalışmaya ayarlandığında izlenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="7346f-110">Makinenin son alınan Parça Çıkış sinyalinden bu yana geçen süre, uyarı eşiğinden büyükse **Makine arızası** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="7346f-111">Makine hala çalışıyorsa bir sonraki **PartOut** sinyali alındığında **Makine devrede** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="7346f-112">Makine, 30 dakika boyunca arızada kalırsa yeni bir **Makine arızası** bildirimi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="7346f-113">**Ekipman kesinti süresi** senaryosu, şu bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="7346f-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="7346f-114">Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7346f-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="7346f-115">Eşlenmiş bir makinenin parça çıkış sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7346f-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="7346f-116">IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7346f-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="7346f-117">Senaryoyu yapılandırmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="7346f-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="7346f-118">Supply Chain Management'ta oturum açın.</span><span class="sxs-lookup"><span data-stu-id="7346f-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="7346f-119">IoT Zekası özellik bayrağını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="7346f-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="7346f-120">Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7346f-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="7346f-121">Ölçümleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7346f-121">Configure the metrics.</span></span> <span data-ttu-id="7346f-122">Daha fazla bilgi için bkz. [Ölçümleri yapılandıma](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="7346f-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="7346f-123">**Üretim denetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7346f-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="7346f-124">**Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7346f-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="7346f-125">**Ekipman kesinti süresi** kutucuğunda **Yapılandır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="7346f-126">Yapılandırma sihirbazı **Ekipman sensörü şema tanımı** sayfası ile başlar.</span><span class="sxs-lookup"><span data-stu-id="7346f-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="7346f-127">Buradaki amaç, Supply Chain Management'ta şemayı IoT iletilerinin JSON biçimiyle eşleşecek şekilde ayarlamaktır.</span><span class="sxs-lookup"><span data-stu-id="7346f-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="7346f-128">Birden çok ileti şeması tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7346f-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="7346f-129">Daha fazla bilgi için bkz. [IoT Hub için ileti şeması biçimleri](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="7346f-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="7346f-130">Bu örnekte ileti yükü, şu biçimde bir toplu ileti içerir:</span><span class="sxs-lookup"><span data-stu-id="7346f-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="7346f-131">Tabloya satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7346f-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="7346f-132">**Şema adı**'nı **Kod** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="7346f-133">**Şema yolu**'nu **/payload[\*]/id** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="7346f-134">**Açıklama**'yı **İleti kodu** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="7346f-135">Tabloya satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7346f-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="7346f-136">**Şema adı**'nı **Zaman damgası** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="7346f-137">**Şema yolu**'nu **/payload[\*]/timestamp** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="7346f-138">**Açıklama**'yı **İleti zaman damgası** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="7346f-139">Tabloya satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7346f-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="7346f-140">**Şema adı**'nı **Değer** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="7346f-141">**Şema yolu**'nu **/payload[\*]/value** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="7346f-142">**Açıklama**'yı **İleti değeri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="7346f-143">İletideki tüm özellikleri tanımlamanız gerekmez, yalnızca ihtiyacınız olanları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="7346f-144">Bu örnekte, **Kök zaman damgası** için bir satır oluşturmadınız.</span><span class="sxs-lookup"><span data-stu-id="7346f-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="7346f-145">**Kök zaman damgası** yolu **/timestamp** olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7346f-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="7346f-146">**Ekipman sensörü şema tanımı** sayfasına gitmek için **İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="7346f-147">**Ekipman kaynak kodu** satırında **Şema adı**'nı **Kod** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="7346f-148">Geçerli değerler, bir açılan tabloda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="7346f-149">**UTC saati** satırında **Şema adı**'nı **Zaman damgası** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="7346f-150">Geçerli değerler, bir açılan tabloda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="7346f-151">**Parça üretildi sinyali** satırında **Şema adı**'nı **Değer** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="7346f-152">Geçerli değerler, bir açılan tabloda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7346f-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="7346f-153">**Ekipman kaynağı kod yapılandırması** sayfası için **İleri**'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="7346f-154">Bu adımda IoT Hub ileti değerlerini Supply Chain Management kaynaklarıyla eşlersiniz.</span><span class="sxs-lookup"><span data-stu-id="7346f-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="7346f-155">**Sinyal Veri Değerleri** tablosuna yeni bir satır ekleyin ve **Değer** sütununa **IoTInt.Machine1225.PartOut** girin.</span><span class="sxs-lookup"><span data-stu-id="7346f-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="7346f-156">**IoTInt.Machine1225.PartOut** değeri, IoT Hub iletisindeki JSON **kod** özelliğinden gelir.</span><span class="sxs-lookup"><span data-stu-id="7346f-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="7346f-157">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-157">Click **Save**.</span></span>
    3. <span data-ttu-id="7346f-158">**İş Kaydı Eşleme** tablosunda **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="7346f-159">**İş kaydı türü** için varsayılan değer otomatik olarak doldurulmuştur ve değiştirmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="7346f-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="7346f-160">**İş kaydı** sütununda, bu sinyal değerinin gönderildiği Supply Chain Management makine kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="7346f-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="7346f-161">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-161">Click **Save**.</span></span>
    6. <span data-ttu-id="7346f-162">**Machine1226** için yeni bir iş kaydı eşlemesi ekleyerek bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="7346f-163">Birden çok sinyal veri değerini Supply Chain Management'ta tek bir kayda eşleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7346f-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="7346f-164">Hangi makineleri işlemek istediğinizi seçmek için **Seçili** sütununu kullanın.</span><span class="sxs-lookup"><span data-stu-id="7346f-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="7346f-165">Tüm sinyal değerlerini tanımlamanız ve tüm makineleri seçmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="7346f-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="7346f-166">**Parça üretildi sinyali yapılandırması** sayfasına gitmek için **İleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="7346f-167">**Sinyal Veri Değerleri** tablosuna bir satır ekleyin ve **Değer**'i **Doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="7346f-168">**Doğru** değeri, IoT Hub iletisindeki JSON **değer** özelliğinden gelir.</span><span class="sxs-lookup"><span data-stu-id="7346f-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="7346f-169">Senaryonuz için gereksinim duyduğunuz kadar değer ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7346f-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="7346f-170">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-170">Click **Save**.</span></span>
20. <span data-ttu-id="7346f-171">**Ekipman kesinti süresi eşiği** sayfasına gitmek için **İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="7346f-172">Listelenen makineler, daha önce sinyal değerlerine eşlenen makinelerdir.</span><span class="sxs-lookup"><span data-stu-id="7346f-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="7346f-173">Bu adımda, bir makinenin arızalı olup olmadığını belirlemek için bir eşik tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="7346f-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="7346f-174">Örneğin eşiği 10 olarak ayarlarsanız, 10 dakika boyunca bir makineden parça çıkışı mesajı yoksa Supply Chain Management bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7346f-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="7346f-175">**Senaryoyu etkinleştir** sayfasına gitmek için **İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="7346f-176">Senaryoyu etkinleştirmek için kaydırıcıyı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="7346f-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="7346f-177">**Son** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-177">Click **Finish**.</span></span>

<span data-ttu-id="7346f-178">Senaryo kurulumu tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="7346f-178">The scenario setup is complete.</span></span> <span data-ttu-id="7346f-179">IoT Zekası, IoT Hub iletilerini otomatik olarak işlemeye başlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="7346f-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="7346f-180">Supply Chain Management'ta **Ürün kalitesi** senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7346f-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="7346f-181">Maddenin özelliği, belirtilen aralığın dışındaysa **Ürün kalitesi** senaryosu bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7346f-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="7346f-182">Örneğin, bir sensör her maddenin ağırlığını IoT Hub'a gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="7346f-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="7346f-183">Supply Chain Management'ta, madde çok ağır veya çok hafifse bir bildirim oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7346f-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="7346f-184">Senaryo şu bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="7346f-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="7346f-185">Uyarının tetiklenmesi için bir Üretim Emri'nin eşlenmiş bir makinede çalışması ve eşlenen toplu iş özniteliğe sahip bir ürün üretmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7346f-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="7346f-186">Toplu iş özniteliğini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7346f-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="7346f-187">IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7346f-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="7346f-188">Supply Chain Management'ta **Üretim gecikmeleri** senaryosunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7346f-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="7346f-189">Üretim iş çıkarma yeteneği bir eşik değerinin altına düşerse **Üretim gecikmeleri** senaryosu bir bildirim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7346f-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="7346f-190">Bu senaryoda, üretilen her madde için IoT Hub'a bir **PartOut** sinyali gönderilir.</span><span class="sxs-lookup"><span data-stu-id="7346f-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="7346f-191">Supply Chain Management'ta sipariş gecikmesi; üretim emrinin çalışması planlanan süre, üretilmesi gereken madde sayısı, işin ne kadar süredir çalıştığı ve **PartOut** sinyali alınma sayısına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7346f-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="7346f-192">İş için **PartOut** sinyallerinin sayısı beklenen eşik değerinin altına düşerse bir gecikme bildirimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7346f-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="7346f-193">Senaryo şu bağımlılıklara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="7346f-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="7346f-194">Uyarının tetiklenmesi için eşlenmiş bir makinede Üretim Emri çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7346f-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="7346f-195">Eşlenmiş bir makinenin parça çıkış sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7346f-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="7346f-196">IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7346f-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="7346f-197">Senaryoyu devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7346f-197">How to disable a scenario</span></span>

<span data-ttu-id="7346f-198">Senaryoyu devre dışı bırakmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="7346f-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="7346f-199">Supply Chain Management'ta **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7346f-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="7346f-200">Senaryoda **Yapılandır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="7346f-201">Son sihirbaz sekmesine ulaşmak için **İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7346f-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="7346f-202">Senaryoyu devre dışı bırakmak için kaydırıcıyı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="7346f-202">Toggle the slider to disable the scenario.</span></span>
