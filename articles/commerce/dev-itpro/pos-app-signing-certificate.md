---
title: Kod imzalama sertifikası ile MPOS .appx dosyasını imzalama
description: Bu makale, kod imzalama sertifikasıyla MPOS oturumunun nasıl imzalandığını açıklamaktadır.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 4cbdfcb5229be2f04531031c80f41f672b2a4747
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169112"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Kod imzalama sertifikası ile MPOS .appx dosyasını imzalama

[!include [banner](../includes/banner.md)]

Modern POS'u (MPOS) yüklemek için, güvenilen bir sağlayıcıdan kod imzalama sertifikasıyla MPOS uygulamasını imzalayıp, MPOS'un geçerli kullanıcının güvenilir kök klasörü altına yüklendiği tüm makinelere aynı sertifikayı yüklemelisiniz.

MPOS uygulamasını sertifikayla imzalamak için **Retail SDK\\Build tool\\Customization.settings** dosyasındaki bu seçeneklerden birini kullanın:

- Azure DevOps derleme adımlarının Güvenli dosya görevi bölümünü ekleyin ve dosya görevini güvenli hale getirmek için sertifikayı karşıya yükleyin. Güvenli dosya görevi çıktı yolu değişkenini, Customization.settings dosyasında parametre olarak kullanın.

    > [!NOTE]
    > Güvenli Dosya görevi parola korumalı bir sertifikayı desteklemez. Bu görevi karşıya yüklemeden önce parolayı kaldırmalısınız. Sertifika, Azure'da güvenli dosya sistemi görevine yüklenmiş olduğundan, yalnızca bu adım için parolayı kaldırabilirsiniz. Ancak, bu işlemin projeniz için doğru eylem olup olmadığını belirlemek için güvenlik uzmanlarıyla parolayı kaldırma konusunu da görüşmelisiniz. Diğer senaryolar için sertifika parolasını kaldırmayın.
- Dosya sistemindeki bir sertifikayı kullanın. Bunu yapmak için bir sertifika yükleyin veya oluşturun ve derlemenin çalıştığı dosya sistemine yerleştirin. Microsoft tarafından barındırılan aracı veya derleme kullanıcısının bu yola ve dosyaya erişimi olmalıdır.
- Mağazada sertifikada arama yapmak ve bu sertifikayla oturum açmak için parmak izini kullanın.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Evrensel Windows Platformu uygulama imzalaması için Güvenli Dosya görevi kullanma

> [!NOTE]
> Sertifikayı depolamak için Azure Key Vault'u kullanabilir ve Modern POS .appx dosyasını ve self servis yükleyicileri imzalamak için Azure Sign aracını kullanabilirsiniz. Örnek işlem hattı kodları ve ek bilgiler için bkz. [Retail self servis paketleri oluşturmak için Azure DevOps'ta derleme işlem hattı ayarlama](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Güvenli Dosya görevi kullanmak, Evrensel Windows Platformu (UWP) uygulama imzalaması için önerilen bir yaklaşımdır. Paket imzalama hakkında daha fazla bilgi için bkz. [Paket imzalamayı yapılandırma](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Bu işlem aşağıdaki resimde gösterilir.

![MPOS uygulama imzalama akışı.](media/POSSigningFlow.png)

> [!NOTE]
> OOB paketi şu anda yalnızca .appx dosyasını imzalamayı destekliyor; MPOIS, RSSU ve HWS gibi farklı self-servis yükleyicileri bu işlem tarafından imzalanmaz. SignTool veya diğer imzalama araçlarını kullanarak el ile imzalamanız gerekir. .appx dosyasını imzalamak için kullanılan sertifika, Modern POS'un yüklü olduğu makinede yüklü olmalıdır.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Sertifikayı Azure Pipelines'ta günlüğe kaydetmek üzere yapılandırma adımları

### <a name="certificate-in-the-file-systemsecure-location"></a>Dosya sistemindeki/güvenli bir konumdaki sertifika

[DownloadFile görevini](/visualstudio/msbuild/downloadfile-task) indirin ve derleme işlemine ilk adım olarak ekleyin. Güvenli Dosya görevini kullanmanın avantajı, derleme işlem hattı başarılı olduğunda, başarısız olduğunda veya iptal edildiğinde bağımsız olarak dosyanın şifrelenmesi ve diske yerleştirilmesidir. Derleme işlemi tamamlandıktan sonra dosya indirme konumundan silinir.

1. Güvenli Dosya görevini indirin ve Azure işlem hattına ilk adım olarak ekleyin. Güvenli Dosya görevini [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile)'dan indirebilirsiniz.
1. Sertifikayı Güvenli Dosya görevine yükleyin ve aşağıdaki görüntüde gösterildiği gibi Çıktı Değişkenleri altında Referans adını ayarlayın.
    > [!div class="mx-imgBorder"]
    > ![Güvenli dosya görevi.](media/SecureFile.png)
1. **Değişkenler** sekmesi altında **Yeni Değişken**'i seçerek Azure Pipelines'da yeni bir değişken oluşturun.
1. Değer alanına değişken için bir ad verin; örneğin, **MySigningCert**.
1. Değişkeni kaydedin.
1. **RetailSDK\\BuildTools**'dan **Customization.settings** dosyasını açın ve **ModernPOSPackageCertificateKeyFile** öğesini işlem hattında oluşturulan (adım 3) değişken adıyla güncelleştirin. Örneğin:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Sertifika parola korumalı değilse bu adım gereklidir. Sertifika parola korumalıysa, aşağıdaki adımlara devam edin.
    
1. MPOS .appx dosyasını sertifikayla imzalarken zaman damgası eklemek istiyorsanız, **Retail SDK\\Geliştirme aracı\\Customization.settings** dosyasını açın ve **ModernPOSPackageCertificateTimestamp** değişkenini zaman damgası sağlayıcısı (ör. `http://timestamp.digicert.com`) ile güncelleştirin.
1. İşlem hattının **Değişkenler** sekmesinde yeni bir güvenli metin değişkeni ekleyin. Adı **MySigningCert.secret** olarak ayarlayın ve sertifikanın parola değerini ayarlayın. Değişkenin güvenliğini sağlamak için kilit simgesini seçin.
1. İşlem hattı için bir **PowerShell Betiği** görevi ekleyin (Güvenli Dosyayı İndirme adımından sonra ve Derleme adımından önce). **Görünen** adı sağlayın ve Tür öğesini **Satır içi** olarak ayarlayın. Aşağıdakileri kopyalayıp komut dosyası bölümüne yapıştırın.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. **RetailSDK\\BuildTools**'dan **Customization.settings** dosyasını açın ve **ModernPOSPackageCertificateThumbprint** öğesini sertifika parmak izi değeriyle güncelleştirin.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Bir sertifikanın parmak izini alma hakkında ayrıntılı bilgi için, [bir sertifikanın parmak izini alma](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint) konusuna bakın. 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>MPOS uygulamasını SDK'da msbuild kullanarak el ile imzalamak için bir sertifika indirme veya oluşturma

İndirilmiş veya oluşturulmuş bir sertifika MPOS uygulamasını imzalamak için kullanılırsa bu durumda, pfx dosya konumuna (**$(SdkReferencesPath)\\appxsignkey.pfx**) işaret etmek için **BuildTools\\Customization.settings** dosyasındaki **ModernPOSPackageCertificateKeyFile** düğümünü güncelleştirin. Örneğin:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Bu durumda sertifika dosyasının adı, **Retail SDK\\Reference** klasöründe bulunan **appxsignkey.pfx**'tir.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>MPOS uygulamasını imzalamak için parmak izini kullanma

MPOS uygulamasını imzalamak için parmak izi kullanırsanız, sertifikayı yerel olarak yükleyin. **BuildTools\\Customization.settings** dosyasındaki **ModernPOSPackageCertificateThumbprint** düğümünde parmak izi değerini güncelleştirin.

Bu seçenek, derleme kullanıcısı yerel bir kullanıcı ise işe yarayacaktır. Ancak, derlemeyi oluşturmak için Azure DevOps aracılarını kullanıyorsanız, aracının imzalama amacıyla sertifikayı kullanabilmesi için sertifika deposuna erişim izni olmayabilir veya derleme makinesinde sertifika yüklü olmayacaktır. Bu durumda geçici çözüm, derleme kullanıcısını yerel kullanıcıyla değiştirmek ve sertifikayı kutuya yüklemektir. Ancak, kutuya yönetici erişiminiz yoksa bu seçenek kullanılamaz.

> [!NOTE]
> Uygulamayı imzalamak için .pfx dosyası veya Güvenli Dosya görevi seçeneği kullanılmışsa, **Customization.settings** öğesindeki **ModernPOSPackageCertificateThumbprint** düğümünü boş bırakın. Parmak izi seçeneği kullanılırsa, **ModernPOSPackageCertificateKeyFile** öğesini boş bırakın. Her iki değer de güncelleştiriliyorsa, derleme başarısız olur.

### <a name="certification-renewal"></a>Sertifika yenileme

### <a name="renew-a-certificate-from-trusted-ca"></a>Sertifikayı güvenilen CA'dan yenileme

Sertifika yenileme işlemi için sertifika yetkilisine (CA) başvurun. Güvenilen bir sertifika için, MPOS tarafında herhangi bir işlem yapılması gerekmez.

### <a name="renew-a-self-signed-certificate"></a>Otomatik olarak imzalanan sertifikayı yenileme

Üretim için Retail SDK'daki mevcut örnek sertifikayı kullanmayın. Yalnızca geliştirme amaçlarıyla kullanılabilir. Contoso sertifikası örneği yenilenemez ve Retail SDK sürüm 10.0.16 veya önceki sürümüne dahil edilen örnek sertifikanın süresi 31 Aralık 2020 tarihinde sona erer. Bu sertifika veya otomatik olarak imzalanan bir sertifika özelleştirilmiş modern bir POS'u imzalamak için kullanılmışsa, Modern POS bu tarihten sonra yüksek olasılıkla doğru şekilde çalışmayacaktır.
 
### <a name="impact"></a>Etki
 
Sizin için yukarıdaki durum geçerli ise, karşılaşacağınız sorun yükleyicinin 31 Aralık 2020'den sonra çalışamayacak olmasıdır. Kullanılan şirket BT ilkelerine bağlı olarak, Modern POS'un çalışması mümkün olmayabilir. Bunu, kuruluşunuza etkisini belirlemek için tarihi geçici olarak gelecekteki bir tarihe değiştirerek sınamanız kritik önem taşır.
 
### <a name="steps-to-determine-the-issue"></a>Sorunu belirleme adımları
 
1.  Bilgisayar saatini 2021 yılındaki bir tarih ve saat olarak değiştirmek için Windows ayarlarını kullanın.
2.  Modern POS'un açılabildiğini, oturum açabildiğinizi ve bir hareketin tamamlanabildiğini doğrulayın.
3.  Modern POS self servis yükleyicisinin çalışıp çalışamadığını ve çalışıyorsa yüklemenin başarıyla tamamlanıp tamamlanmadığını doğrulayın.
4.  Windows saati ayarlarını doğru tarih ve saate döndürün.
 
Bu adımların tümünü sorun olmadan tamamlayabiliyorsanız, geçerli sertifika üzerinde 31 Aralık 2020 tarihinden sonra işlem yapabilirsiniz.  
 
### <a name="steps-going-forward"></a>Bundan sonraki adımlar 

Önceden kullanılmış sertifikayı yenilemeniz önemle önerilir. Yeni bir sertifika almanız kesinlikle önerilir. Bunu yapmak için aşağıdaki eylemlerden birini gerçekleştirmelisiniz:
 
- **Tercih Edilen** - Güvenilir bir sertifika yetkilisinden kod imzalama sertifikası edinin.

- **Tercih Edilmeyen** - Kullanmak için kendinden imzalı bir kod imzalama sertifikası oluşturun. Bu genellikle bir etki alanı içinde geliştirme amacıyla kullanılır ve üretim için önerilmez. 

- **Geçici çözüm olarak kullanılabilir** - Yenilenen Contoso kod imzalama sertifikasını kullanın. Bu genellikle test amacıyla kullanılır, bu nedenle üretim sırasında dağıtılması önerilmez.
 
Daha sonra, yukarıdaki eylemlerden birinden elde edilen bu sertifika kullanılarak imzalanmış, yeni bir özel Modern POS paketi oluşturun. Sertifikaya bağlı olarak aşağıdaki adımlardan biri izlenmelidir:
 
- Yeni bir güvenilen sertifika (veya otomatik olarak imzalanan sertifika) kullanılıyorsa, her cihaza yeni bir sertifika yüklemeniz gerekecektir. Bundan sonra, yeni oluşturulan Modern POS paketini (yükleyici) edinmeniz, varolan uygulamayı kaldırmanız ve sonra yeni Modern POS paketini yeniden yüklemeniz gerekir. Her cihazda Modern POS'un cihaz etkinleştirmesini gerçekleştirmeniz gerekir.

- Yenilenen Contoso sertifikasını kullanıyorsanız, yeni sertifikayı her cihaza yüklemeniz ve Modern POS paketini (yükleyici) yüklemeniz gerekir. Kaldırmanız gerekli değildir, ancak cihaza yeniden yüklemeniz gerekir. Modern POS'un cihaz etkinleştirmesi gerekli olmayacaktır. Bu seçenek geçici bir çözümdür. Bu seçeneği yalnızca yeniden etkinleştirmeyi önlemek ve yeni bir güvenilen sertifika edinmeden önce sorunu çözmek için kullanın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
