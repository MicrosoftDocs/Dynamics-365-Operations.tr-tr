---
title: "Perakende kanalı için mali tümleştirme"
description: "Bu konu, Retail POS için mali entegrasyon genel görünümünü sağlar."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: tr-tr
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="06423-103">Perakende kanalı için mali tümleştirme</span><span class="sxs-lookup"><span data-stu-id="06423-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06423-104">Bu konu Microsoft Dynamics 365 for Retail'da kullanılabilir olan mali tümleştirme işlevinin genel açıklamasıdır.</span><span class="sxs-lookup"><span data-stu-id="06423-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="06423-105">Mali tümleştirme işlevi, Perakende sektöründe dolandırıcılığı önlemeyi amaçlayan mali yerel yasaları desteklemek için tasarlanmış bir işlevdir.</span><span class="sxs-lookup"><span data-stu-id="06423-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="06423-106">Mali tümleştirme kullanarak kapsanabilen tipik senaryolar:</span><span class="sxs-lookup"><span data-stu-id="06423-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="06423-107">Mali makbuz yazdırmak ve bunu müşteriye vermek.</span><span class="sxs-lookup"><span data-stu-id="06423-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="06423-108">Satışla ilgili bilgilerin gönderilmesinin ve POS üzerindeki iadelerin yetkili tarafından sağlanan harici bir hizmete gönderilmesinin güvenliğini sağlama.</span><span class="sxs-lookup"><span data-stu-id="06423-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="06423-109">Yetkili tarafından yetkilendirilmiş bir dijital imzayla veri koruması kullanma.</span><span class="sxs-lookup"><span data-stu-id="06423-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="06423-110">Bu konu, kullanıcılar aşağıdaki görevleri gerçekleştirebilsin diye mali entegrasyon kurulumu ayarlamak için yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="06423-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="06423-111">Kaydetme, dijital imzalar ve mali verilerin güvenli gönderimi gibi mali kayıt amaçları için kullanılan mali aygıt ya da hizmetler olan mali konnektörler konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="06423-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="06423-112">Mali belge oluşturma algoritması ve bir çıktı yöntemi tanımlayan belge sağlayıcı konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="06423-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="06423-113">Adımlar sıralaması ve her adımda kullanılan bir grup bağlayıcı tanımlayan mali kayıt işlemi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="06423-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="06423-114">POS işlevsellik profilleri için mali kayıt işlemleri atayın.</span><span class="sxs-lookup"><span data-stu-id="06423-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="06423-115">Donanım profilleri (yerel mali bağlayıcılar için) veya (diğer mali bağlayıcı türleri için) POS işlevsellik profillerine bağlayıcı teknik profilleri atayın.</span><span class="sxs-lookup"><span data-stu-id="06423-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="06423-116">Mali tümleştirme yürütme akışı</span><span class="sxs-lookup"><span data-stu-id="06423-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="06423-117">Aşağıdaki senaryo, ortak mali tümleştirme yürütme akışı gösterir.</span><span class="sxs-lookup"><span data-stu-id="06423-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="06423-118">Mali kayıt sürecinin başlatılması.</span><span class="sxs-lookup"><span data-stu-id="06423-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="06423-119">Perakende hareketinin tamamlanmasından sonrası gibi mali kayıt gerekli olduğu bazı eylemler gerçekleştirdikten sonra, mali kayıt işlemi geçerli POS işlevsellik profili ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="06423-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="06423-120">Mali bağlayıcı arayın.</span><span class="sxs-lookup"><span data-stu-id="06423-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="06423-121">Mli kayıt işlemindeki her mali kayıt adımı için sistem mali bağlayıcı listesi eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="06423-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="06423-122">Bu bağlayıcılar, belirtilen bağlayıcı grubuna dahil olan işlevsel profile sahiptir; mevcut donanım profiliyle (yalnızca **Yerel**e eşit olan bağlayıcı türü için) veya geçerli POS işlevsellik profili (diğer bağlayıcı türleri için) ilişkili bir teknik profil bağlayıcı listesine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="06423-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="06423-123">Mali tümleştirme gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="06423-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="06423-124">Sistem, bulunan bağlayıcıyla ilişkili bir derleme tarafından tanımlanan tüm gerekli olan eylemleri yürütür.</span><span class="sxs-lookup"><span data-stu-id="06423-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="06423-125">Bu işlev profili ve bu bağlayıcı için önceki adımda bulunan teknik profilin ayarlarına göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="06423-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="06423-126">Mali tümleştirme kullanmadan önce kurulum gerekir</span><span class="sxs-lookup"><span data-stu-id="06423-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="06423-127">Mali tümleştirme işlevini kullanmadan önce aşağıdaki ayarları tanımlarsınız:</span><span class="sxs-lookup"><span data-stu-id="06423-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="06423-128">Mali işlev profili numarası için **Perakende parametreleri**nde numara sırasını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="06423-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="06423-129">Aşağıdaki referanslar için **Perakende paylaşılan parametreleri** sayfasında numara serileri tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="06423-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="06423-130">Mali teknik profil numarası</span><span class="sxs-lookup"><span data-stu-id="06423-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="06423-131">Mali bağlayıcı grubu numarası</span><span class="sxs-lookup"><span data-stu-id="06423-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="06423-132">Kayıt işlemi numarası</span><span class="sxs-lookup"><span data-stu-id="06423-132">Registration process number</span></span>

- <span data-ttu-id="06423-133">**Mali bağlayıcı**'yı **Perakende > Kanal Kurulumu > Mali tümleştirme > Mali bağlayıcılar**'da oluşturun; mali tümleştirme amaçları için kullanmayı planladığınız her aygıt veya hizmet için.</span><span class="sxs-lookup"><span data-stu-id="06423-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="06423-134">Tüm mali bağlayıcılar için **Mali belge sağlayıcı**'yı **Perakende > Kanal Kurulum > Mali tümleştirme > Mali belge sağlayılar**'da oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06423-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="06423-135">Veri eşleme mali belge sağlayıcının bir parçası olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="06423-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="06423-136">Aynı bağlayıcı için farklı veri eşlemeleri (örneğin, özel durum düzenlemeleri), farklı mali belge sağlayıcıları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="06423-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="06423-137">Her mali belge sağlayıcısı için **Bağlayıcı işlev profili**'nde **Perakende > Kanal kurulumu > Mali tümleştirme > Bağlayıcı işlev profilleri** oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06423-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="06423-138">Bir bağlayıcı adı seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-138">Select a connector name.</span></span>
  - <span data-ttu-id="06423-139">Bir belge sağlayıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-139">Select a document provider.</span></span>
  - <span data-ttu-id="06423-140">**Hizmet Kurulumu** sekmesinde KDV oranları ayarlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="06423-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="06423-141">KDV kodu eşlemesi ve ödeme türü eşlemesini **Veri eşleme** sekmesinde belirtin.</span><span class="sxs-lookup"><span data-stu-id="06423-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="06423-142">Örnekler</span><span class="sxs-lookup"><span data-stu-id="06423-142">Examples</span></span> 

  |  | <span data-ttu-id="06423-143">Biçim</span><span class="sxs-lookup"><span data-stu-id="06423-143">Format</span></span> | <span data-ttu-id="06423-144">Örnek</span><span class="sxs-lookup"><span data-stu-id="06423-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="06423-145">KDV oranı ayarları</span><span class="sxs-lookup"><span data-stu-id="06423-145">VAT rates settings</span></span> | <span data-ttu-id="06423-146">değer: VATrate</span><span class="sxs-lookup"><span data-stu-id="06423-146">value : VATrate</span></span> | <span data-ttu-id="06423-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="06423-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="06423-148">KDV kodları eşlemesi</span><span class="sxs-lookup"><span data-stu-id="06423-148">VAT codes mapping</span></span> | <span data-ttu-id="06423-149">VATcode : değer</span><span class="sxs-lookup"><span data-stu-id="06423-149">VATcode : value</span></span> | <span data-ttu-id="06423-150">vat20: 1, vat18: 2</span><span class="sxs-lookup"><span data-stu-id="06423-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="06423-151">Ödeme türleri eşlemesi</span><span class="sxs-lookup"><span data-stu-id="06423-151">Tender types mapping</span></span> | <span data-ttu-id="06423-152">TenderTyp: değer</span><span class="sxs-lookup"><span data-stu-id="06423-152">TenderTyp : value</span></span> | <span data-ttu-id="06423-153">Nakit: 1, Kart: 2</span><span class="sxs-lookup"><span data-stu-id="06423-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="06423-154">**Mali bağlayıcı grupları**'nı **Perakende > Kanal kurulumu > Mali tümleştirme > Mali bağlayıcı grubu**nda oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06423-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="06423-155">Bağlayıcı grubu, aynı işlevleri gerçekleştiren ve mali kayıt sürecinde aynı aşamada kullanılan mali bağlayıcılarla ilişkili işlevsel profillerin alt grubudur.</span><span class="sxs-lookup"><span data-stu-id="06423-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="06423-156">Konnektör grubuna işlevsel profiller ekleyin.</span><span class="sxs-lookup"><span data-stu-id="06423-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="06423-157">**İşlevsel profiller** sayfasında **Ekle**'ye tıklayın ve profil numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="06423-158">İşlev profili kullanımı askıya almak istiyorsanız, **Devre dışı bırakma** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="06423-159">Bu değişikliği yalnızca geçerli bağlayıcı grubu etkiler.</span><span class="sxs-lookup"><span data-stu-id="06423-159">This change affects the current connector group only.</span></span> <span data-ttu-id="06423-160">Bağlayıcı başka gruplarda aynı işlev profili kullanarak devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06423-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="06423-161">Bağlayıcı grup içinde her mali connector yalnızca bir işlev profili olabilir.</span><span class="sxs-lookup"><span data-stu-id="06423-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="06423-162">Her mali bağlayıcı için **Bağlayıcı teknik profili**'nde **Perakende > Kanal kurulumu > Mali tümleştirme > Bağlayıcı teknik profilleri** oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06423-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="06423-163">Bir bağlayıcı adı seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-163">Select a connector name.</span></span>
  - <span data-ttu-id="06423-164">Bir bağlayıcı türü seçin:</span><span class="sxs-lookup"><span data-stu-id="06423-164">Select a connector type:</span></span> 
      - <span data-ttu-id="06423-165">**Yerel** - Bu türü fiziksel aygıt ya da yerel makine üzerinde yüklü uygulamalar için ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06423-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="06423-166">**Dahili** - Bu türü, mali aygıt ve Retail sunucusuna bağlı servisler için seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="06423-167">**Harici** - Vergi dairesi tarafından sağlanan bir web portalı gibi harici mali hizmetler için.</span><span class="sxs-lookup"><span data-stu-id="06423-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="06423-168">**Bağlantı** sekmesinde ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="06423-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="06423-169">İşlevsel ve teknik profilleri için daha önce yüklenen konfigürasyonun güncelleştirilmiş bir sürümü yüklenir.</span><span class="sxs-lookup"><span data-stu-id="06423-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="06423-170">Uygun bir bağlayıcı veya belge sağlayıcısı zaten kullanılıyorsa, size bildirilir.</span><span class="sxs-lookup"><span data-stu-id="06423-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="06423-171">Varsayılan olarak, işlev ve teknik profillerinde el ile yaptığınız tüm değişiklikler depolanır.</span><span class="sxs-lookup"><span data-stu-id="06423-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="06423-172">Bu profilleri varsayılan parametreler yapılandırma kümesiyle geçersiz kılmak için **Güncelleştir**'e tıklayın: **Bağlayıcı işlev profilleri** sayfası ve **Bağlayıcı teknik profilleri** sayfasında.</span><span class="sxs-lookup"><span data-stu-id="06423-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="06423-173">**Mali kayıt işlemi**'ni **Perakende > Kanal kurulumu > Mali tümleştirme > Mali kayıt işlemleri**'nde, mali tümleştirmenin benzersiz her işlemi için oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06423-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="06423-174">Bir kayıt işlemi, kayıt adımları ve her adımda kullanılan bağlayıcı grubu dizisi ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="06423-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="06423-175">İşlem için kayıt adımları ekleyin:</span><span class="sxs-lookup"><span data-stu-id="06423-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="06423-176">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06423-176">Click **Add**.</span></span>
      - <span data-ttu-id="06423-177">Bir bağlayıcı türü seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="06423-178">Bu alan, sistemin bağlayıcının teknik profilinde arama yapacağı yeri belirtir: **Yerel** bağlayıcı türü için donanım profilleri veya diğer mali bağlayıcı türleri için POS işlevsellik profilleri.</span><span class="sxs-lookup"><span data-stu-id="06423-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="06423-179">Bağlayıcı grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="06423-180">**Doğrula**'ya tıklatıp kayıt işlemi yapısının bütünlüğünü denetleyin.</span><span class="sxs-lookup"><span data-stu-id="06423-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="06423-181">Doğrulamaların aşağıdaki durumlarda yapılması önerilir:</span><span class="sxs-lookup"><span data-stu-id="06423-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="06423-182">POS işlev profillerini ve donanım profillerini bağlama dahil tüm ayarlar tamamlandıktan sonra yeni kayıt işlemi için.</span><span class="sxs-lookup"><span data-stu-id="06423-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="06423-183">Güncelleştirmeleri varolan bir kayıt işlemine yapıldıktan sonra.</span><span class="sxs-lookup"><span data-stu-id="06423-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="06423-184">Mali kayıt süreçlerini POS işlevsellik profillerine **Perakende > Kanal Kurulum > POS Kurulum > POS profilleri > İşlevsellik profilleri**'nde bağlayın.</span><span class="sxs-lookup"><span data-stu-id="06423-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="06423-185">**Düzenle**'ye tıklayın ve **İşlem numarası**'nı **Mali kayıt işlemini** sekmesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="06423-186">Donanım profillerine bağlayıcı teknik profillerini **Perakende > Kanal Kurulum > POS Kurulum > POS profilleri > Donanım profilleri**'nde bağlayın.</span><span class="sxs-lookup"><span data-stu-id="06423-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="06423-187">**Düzenle**'ye tıklayın, ardından **Yeni**'yi **Mali teknik profil** sekmesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="06423-188">Bağlayıcı teknik profilini **Profil numarası** alanında seçin.</span><span class="sxs-lookup"><span data-stu-id="06423-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="06423-189">Çok sayıda teknik profilleri, bir donanım profiline ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06423-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="06423-190">Ancak, herhangi bir grup bağlayıcıyla birden çok kesişimi olan donanım profili varsa, bu desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="06423-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="06423-191">Yanlış ayarları önlemek için tüm donanım profilleri güncelleştirildikten sonra kayıt işlemini doğrulamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="06423-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

