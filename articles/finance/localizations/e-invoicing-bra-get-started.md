---
title: Brezilya için Elektronik faturalamayı kullanmaya başlama
description: Bu konu, Finance ve Supply Chain Management'ta Brezilya için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 82bbf806d207af0b15406e4bec516420db7f2c06
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984865"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Brezilya için Elektronik faturalamayı kullanmaya başlama 

[!include [banner](../includes/banner.md)]

Bu konu, Brezilya için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Bu konu Regulatory Configuration Services'da (RCS) ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder ve [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunda açıklanan adımları tamamlar.

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Brezilya NF-e (BR) elektronik faturalama özelliği için ülkeye özel yapılandırma

**Brezilya NF-e (BR) elektronik faturalama özelliğindeki** parametrelerden bazıları varsayılan değerlerle yayımlanır. Değerleri gözden geçirin ve gerekirse, elektronik faturalama özelliğini servis ortamına dağıtmadan önce iş operasyonlarınızı daha iyi yansıtması için değerleri güncelleştirin.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Elektronik Faturalama özelliği için ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, oluşturduğunuz **Brezilya NF-e (BR)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, kılavuzda, **Gönder**'i seçin ve **Düzenle**'yi seçin.
5. **Eylemler** sekmesinde, **Eylemler** alan grubunda **(Önizleme) xml belgesini imzala** eylemini seçin.
6. **Parametreler** alan grubunda **Sertifika adı**'nı seçin ve **değer** alanına Key Vault parametreniz ile ilişkilendirilen sertifikanın adını girin.
7. **Eylemler** sekmesinde, **Eylemler** alan grubunda **(Önizleme) Brezilya SEFAZ hizmetini ara** eylemini seçin.
8. **Parametreler** alan grubunda **URL adresi** parametresi seçin.
9. **Değer** alanında, gerekiyorsa durumunuz için SEFAZ belgeleri tarafından yayınlanan Web hizmetlerinin URL'sini gözden geçirip güncelleştirin ve sonra **Kaydet**'i seçin.
10. **Uygulanabilirlik kuralları** sekmesindeki **Uygulanabilirlik kuralının ayarlanması** alan grubunda, Web Hizmetleri URL'sinin başvuruda bulunduğu aynı durum için gerekirse **durum** alanı kriterini gözden geçirip güncelleştirin.
11. **Kaydet**'i seçip sayfayı kapatın.
12. Elektronik faturalama özelliğini Service ortamına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Brezilya NF-e (BR) elektronik faturalama özelliği için uygulama kurulumunun ülkeye özel yapılandırması

Uygulama kurulumunu Finance veya Supply Chain Management bağlı uygulamanıza dağıtmadan önce bu adımları tamamlayın.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Uygulama kurulumunu ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, **Brezilya NF-e (BR)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, **Uygulama kurulumu**'nu seçin ve **bağlı uygulama** alanında, dağıtma işlemini yapmak istediğiniz uygulamayı seçin.
5. **Tablo adı** alanında, **Mali belge başlığı** öğesinin seçili olduğunu doğrulayın.
6. **Yanıt türlerini** seçin ve ardından **yeni**'yi seçin.
7. **Yanıt türü** alanında, sabit değer olarak "yanıt"ı girin ve **Açıklama** alanına "Açıklama" yazın.
8. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
9. **Model eşleme** alanında, **Yanıt iletisinden model eşlemesi** ile **(Önizleme)Yanıt iletisi içe aktarma biçimi**'ni seçin ve ardından **Kaydet**'i seçin.
10. **Yanıt türü** alanında, **Yanıt türü** alanında sabit değer olarak "ResponseData"yı girin ve **Açıklama** alanına "Açıklama" yazın.
11. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
12. **Model eşleme** alanında, **Yanıt verisi içe aktarma** ile **(Önizleme)NF-e yanıt verisi içe aktarma biçimi (BR)**'ni seçin ve ardından **Kaydet**'i seçin.
13. Uygulama kurulumunu Finance veya Supply Chain bağlı uygulamasına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Brezilya NFS-e ABRASF Curitiba (BR) elektronik faturalama özelliği için ülkeye özel yapılandırma

**Brezilya NFS-e ABRASF Curitiba (BR) elektronik faturalama özelliğindeki** parametrelerden bazıları varsayılan değerlerle yayımlanır. Gözden geçirin ve gerekirse, elektronik faturalama özelliğini servis ortamına dağıtmadan önce iş operasyonu ihtiyaçlarınıza daha iyi uyması için değerleri güncelleştirin.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Elektronik Faturalama özelliği için ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, oluşturduğunuz **Brezilya NFS-e ABRASF Curitiba (BR)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın ve **Kurulumlar** sekmesinde, kılavuzda, **Gönder** seçeneğini belirleyin.
4. **Düzenle** öğesini seçin ve **Eylemler** sekmesinde, **Eylemler** alan grubunda, ilk **(Önizleme) xml belgesini imzala** seçeneğini belirleyin.
5. **Parametreler** alan grubunda **Sertifika adı** öğesini seçin.
6. **Değer** alanına, Key Vault parametreniz ile ilişkilendirilen sertifikanın adını girin.
7. **Eylemler** alan grubunda, ikinci **(Önizleme) xml belgesini imzala** seçeneğini belirleyin.
8. **Parametreler** alan grubunda **Sertifika adı** öğesini seçin.
9. **Değer** alanına, Key Vault parametreniz ile ilişkilendirilen sertifikanın adını girin.
10. **Eylemler** sekmesinde, **Eylemler** alan grubunda **(Önizleme) Brezilya SEFAZ hizmetini ara** eylemini seçin.
11. **Parametreler** alan grubunda **URL adresi** parametresi seçin.
12. **Değer** alanında, gerekiyorsa durumunuz için Curitiba şehrinin vergi departmanı tarafından yayınlanan Web hizmetlerinin URL'sini gözden geçirip güncelleştirin ve sonra **Kaydet**'i seçin.
13. **Ayarlar** sekmesinde, kılavuzda, **Sorgula**'yı seçin ve ardından **Düzenle**'yi seçin.
14. **Eylemler** sekmesinde, **Eylemler** alan grubunda **(Önizleme) Brezilya SEFAZ hizmetini ara** eylemini seçin.
15. **Parametreler** alan grubunda **URL adresi** parametresi seçin.
16. **Değer** alanında, gerekiyorsa Curitiba şehrinin vergi departmanı tarafından yayınlanan Web hizmetlerinin URL'sini gözden geçirip güncelleştirin.
17. **Kaydet**'i seçip sayfayı kapatın.
18. Elektronik faturalama özelliğini Service ortamına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Brezilya NFS-e ABRASF Curitiba (BR) elektronik faturalama özelliği için uygulama kurulumunun ülkeye özel yapılandırması

Uygulama kurulumunu Finance veya Supply Chain Management bağlı uygulamanıza dağıtmadan önce bu adımları tamamlayın.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Uygulama kurulumunu ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, **Brezilya NFS-e ABRASF Curitiba (BR)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın ve **Kurulumlar** sekmesinde, **Uygulama kurulumu** seçeneğini belirleyin.
4. **Bağlı uygulama** alanında, dağıtma işlemini yapmak istediğiniz uygulamayı seçin.
5. **Tablo adı** alanında, Mali belge başlığı öğesinin seçili olduğunu doğrulayın.
6. **Yanıt türlerini** seçin ve **yeni**'yi seçin.
7. **Yanıt türü** alanında, sabit değer olarak "ABRASFCuritibaSubmitResponse"'u girin ve **Açıklama** alanına "Açıklama" yazın.
8. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
9. **Model eşleme** alanında, **Yanıt iletisini içe aktarma** ile **(Önizleme)NFS-e ABRASF Curitiba yanıt iletisi içe aktarma (BR)**'yı seçin ve ardından **Kaydet**'i seçin.
10. **Yanıt türü** alanında, **Yanıt türü** alanında sabit değer olarak "ABRASFCuritibaSubmitResponseData"yı ve **Açıklama** alanına "Açıklama" yazın.
11. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
12. **Model eşleme** alanında, **Yanıt verisi içe aktarma** ile **(Önizleme) NFS-e ABRASF yanıt verisi içe aktarma biçimi (BR)**'ni seçin ve ardından **Kaydet**'i seçin.
13. **Yanıt türü** alanında, **Yanıt türü** alanında "ABRASFCuritibaInquireResponse"u girin ve **Açıklama** alanına "Açıklama" yazın.
14. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
15. **Model eşleme** alanında, **Yanıt iletisini içe aktarma** ile **(Önizleme) NFS-e ABRASF Curitiba yanıt iletisi içe aktarma (BR)**'yı seçin.
16. **Kaydet**'i seçip sayfayı kapatın.
17. Uygulama kurulumunu Finance veya Supply Chain bağlı uygulamasına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="privacy-notice"></a>Gizlilik bildirimi
**NF-e Federal-Brezilya elektronik faturası (BR)** ve **NFS-e-Brezilya Servis (şehir) elektronik faturası** özelliklerinin etkinleştirilmesi, kuruluş vergi kayıt kodu dahil olmak üzere, sınırlı verilerin gönderilmesini gerektirebilir. Bu veriler, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici olarak, **NF-e Federal-Brezilya elektronik faturası (BR)** ve **NFS-e-Brezilya Servis (şehir) elektronik faturası** özelliklerini etkinleştirebilir veya devre dışı bırakabilirsiniz. Aşağıdaki adımlar, bunu nasıl yapacağınızı gösterir: 

1. **Kuruluş yönetimi** > **Kurulum** > **Elektronik belge parametreleri** bölümüne gidin. 
2. **Özellikler** sekmesinde, **NF-e Federal-Brezilya elektronik faturası (BR)** veya **NFS-e-Brezilya servis (şehir) elektronik faturası** özelliğini içeren satırı seçin ve özelliği seçin. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
