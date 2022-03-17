---
title: Hizmet ortamları
description: Bu konu, Elektronik faturalama için hizmet ortamları hakkında bilgi sağlayıp bunları kurmayı açıklar.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a8a135098f71e1413cd20ff8ad4003f090ae3407
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371799"
---
# <a name="service-environments"></a>Hizmet ortamları

[!include [banner](../includes/banner.md)]

Hizmet ortamları, Genelleştirme özellikleri ve karşılık gelen Elektronik Faturalama hizmetinde işlenen belgeleri desteklemek için oluşturulan mantıksal bölümlerdir. Güvenlik gizli dizileri ve dijital sertifikalar ve erişim izinleri (idare), hizmet ortamı düzeyinde konfigüre edilmelidir.

İhtiyaç duyduğunuz sayıda hizmet ortamı oluşturabilirsiniz. Oluşturduğunuz tüm servis ortamları birbirinden bağımsızdır. En iyi yöntem olarak, en azından iki servis ortamı oluşturmanızı öneririz:

- Biri ana geliştirme ve doğrulama amaçları içindir. Bu ortam genellikle bir kullanıcı kabul testi (UAT) ortamıdır.
- Bir ortam da üretim amaçları içindir. Bu ortam genellikle bir üretim ortamıdır.

Bu bölümleme türü, üretime geçmeden önce, e-faturalama işlemlerinin sanal alanda doğrulandığından ve özelleştirildiklerinden emin olmanıza yardımcı olur.

Hizmet ortamlarının, Regulatory Configuration Service (RCS) içinde oluşturulup tutulması gerekir. Ardından, hazır olduklarında Elektronik Faturalama hizmetine yayımlanabilirler. Yayımlama işlemi, RCS örneğinden alınan hizmet ortamı parametrelerini Elektronik Faturalama hizmetine gönderir.

Yeni bir hizmet ortamı oluşturduktan sonra veya mevcut bir hizmet ortamını oluşturduktan sonra (örneğin kullanıcı veya Microsoft Azure Key Vault gizli dizileri ekleme ya da çıkarma) yayımlama işlemini tamamlamazsanız değişiklikler etkili olmaz. Yayımlanan ortamlara yalnızca Dynamics 365 Finance veya Dynamics 365 Supply Chain Management aracılığıyla erişilebilir.

## <a name="service-environment-statuses"></a>Hizmet ortamı durumları

Hizmet ortamları, durumları ile yönetilebilir. Bir ortamın durumunu, **Hizmet ortamları** sayfasında görüntüleyebilirsiniz. Aşağıdaki durumlar mevcuttur:

- **Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.
- **Yayınlandı** – Ortam Elektronik Faturalama hizmeti içinde yayınlanmıştır.
- **Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.

## <a name="users"></a>Kullanıcılar

Her bir hizmet ortamı, Elektronik Faturalama eklentilerinde Finance veya Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.

## <a name="applications"></a>Başvurular

Bazı senaryolarda, Finance veya Supply Chain Management dışındaki uygulamaların, elektronik olarak işlenmek üzere e-bir belge göndermek veya bir belgenin gönderme durumu gibi bilgileri almak için Elektronik Faturalama hizmetine bağlanması gerekebilir. Bu senaryolarda, uygulamanın uygulama listesinde tanımlı olması gerekir. Bu şekilde, Elektronik Faturalama hizmetine erişimi olur. Uygulamanın aynı zamanda Azure Active Directory'de (Azure AD) uygulama olarak kayıtlı olması ve tanımlamak için nesne kimliği kullanılması gerekir. 

Microsoft, Elektronik Faturalama hizmetine bağlanabilecek uygulamalar üzerinde yüksek düzeyde güvenlik denetimi gerektirdiğinden, <DGXRegulatoryservicesengineering@service.microsoft.com> adresinden Microsoft'la iletişime geçmeniz gerekir ve uygulamanızla ilgili aşağıdaki ayrıntıları sağlayın:

- Azure AD kiracı kodu
- Microsoft Dynamics Lifecycle Services (LCS) ortam kimliği
- Uygulama Kimliği (istemci kimliği)
- Nesne kodu
- Gerekçelendirme ve uygulamanın yüksek düzey açıklaması

Microsoft isteği değerlendirir ve Elektronik faturalamayla çalışabildiğinden emin olmak için uygulamayı güvenlik kaydına kaydeder.

## <a name="number-sequences"></a>Numara serileri

Senaryolarınız numara serileri gerektiriyorsa (örneğin, dosya adlarında), belirli bir ortam için tanımlanan, ancak Genelleştirme özellikleri veya belirli bir Genelleştirme özelliği üzerinden kullanılabilecek numara serilerini kullanabilirsiniz. Bir numara serisi tanımlandıktan sonra, bu kodu değişkenler ve işlem ardışık düzenleri ile kullanabilirsiniz. Kullanımını izlemek için, **Numara sıraları** sayfasında, **Kullanımda** parametresi için **Geçerli** değerini arayın.

### <a name="working-with-number-sequences"></a>Numara serileriyle çalışma
**Numara serileri** sayfasında: 

- Numara serisi oluşturmak için **Yeni**'yi seçin. Ardından bir ad ve açıklama girin. 
- Artık kullanılmıyorsa, numara serisini silmek için **Sil**'i seçin.
- Değişiklikleri numara sırasına yayımlamak için eylem bölmesinde **Yayımla** seçeneğini belirlemeniz gerekmez. Güncelleştirme otomatik olarak gerçekleştirilir.

## <a name="create-a-key-vault-reference"></a>Key Vault referansı oluşturma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ortam kurulumu** sayfasındaki Eylem bölmesinde **Hizmet ortamları**'nı seçin.
4. **Hizmet ortamları** sayfasında, Eylem Bölmesi'nde **Key Vault parametreleri**'ni seçin.
5. **Key Vault parametreleri** sayfasında, Key Vault referansı oluşturmak için **Yeni**'yi seçin.
6. **Ad** alanına, Key Vault başvurusunun adını girin.
7. **Açıklama** alanına bir açıklama girin.
8. **Key Vault URI** alanına, anahtar kasasından (`https://<your key vault>.vault.azure.net/`) Key Vault URI'yi girin. Daha fazla bilgi için bkz. [Azure portalında Azure Key Vault oluşturma](e-invoicing-create-azure-key-vault-azure-portal.md).
9. **Kaydet**'i seçin.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Depolama hesabı gizli belirteci için bir parola oluşturma

1. **Key Vault parametreleri** sayfasında, önceki yordamda oluşturduğunuz Key Vault başvurusunu seçin ve sonra **Sertifikalar** bölümünde **Ekle**'yi seçin.
2. **Ad** alanına depolama hesabı gizli dizisinin adını girin. Bu ad, depolama paylaşılan erişim imzası (SAS) belirtecini tutan Key Vault gizli dizisi adıyla eşleşmelidir. Daha fazla bilgi için bkz. [Azure portalında Azure depolama hesabı oluşturma](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. **Açıklama** alanına bir açıklama girin.
4. **Tür** alanında **Gizli Dizi**'yi seçin.
5. **Kaydet**'i seçin.
    
## <a name="create-a-service-environment"></a>Hizmet ortamı oluşturma

1. **Hizmet ortamları** sayfasında, hizmet ortamı oluşturmak için **Yeni**'yi seçin.
2. **Ad** alanına Elektronik faturalama ortamının adını girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken depolama hesabı gizli dizisinin adını seçin.
5. **Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.
6. **Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin. 
7. **E-posta** alanına kullanıcının e-posta adresini girin.
8. **Kaydet**'i seçin.
9. Eylem Bölmesi'nde, ortamı Elektronik Faturalama hizmetine yayınlamak için **Yayınla**'yı seçin. **Durum** alanının değeri **Yayınlandı** olarak değiştirildiğini doğrulayın.
