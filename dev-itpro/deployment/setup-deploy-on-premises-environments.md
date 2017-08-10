---
title: "Şirket içi ortamlar ayarlama ve dağıtma"
description: "Bu konu bir şirket içi ortamın nasıl planlanacağını, kurulacağını ve dağıtılacağına dair bilgi sağlar."
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: tr-tr
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Şirket içi ortamlar ayarlama ve dağıtma

Bu belge Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi) dağıtımınızı planlamayı, alt yapıyı oluşturmayı ve dağıtımını yapmayı açıklar.

## <a name="finance-and-operations-components"></a>Finance and Operations bileşenleri

Finance and Operations uygulaması üç an bileşenden oluşur:

- Uygulama Nesne Sunucusu (AOS)
- Business Intelligence (BI)
- Mali Raporlama/Yönetim Raporlayıcısı

Bu bileşenler aşağıdaki sistem yazılımına bağlıdır:

- Microsoft Windows Server 2016
- Aşağıdaki özelliklere sahip olan Microsoft SQL Server 2016 SP1:

    - Tam metin dizini arama etkindir.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Tam Metin Arama etkin değilse, uygulama çalışmaz.

- SQL Server Management Studio
- Tek Microsoft Azure Service Fabric
- Windows PowerShell 5.0 veya üzeri
- Windows Server 2016 üzerinde Active Directory Federation Services (AD FS)

  Etki alanı denetleyicisi 2012 R2 veya daha büyük etki alanı işlev düzeyine sahip Windows Server 2012 R2 veya üzeri olmalıdır

  Etki alanı işlev düzeyleri hakkında daha fazla bilgi için bakınız: 
  - [Active Directory İşlevsellik düzeyleri nedir](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Active Directory Etki alanı hizmetleri işlev düzeyini anlamak](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations bitleri Microsoft Dynamics Lifecycle Services (LCS) üzerinden dağıtılır. Dağıtım yapabilmeden önce [Kurumsal Anlaşmalar](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) kanalı üzerinden lisans anahtarları satın almalı LCS içerisinde bir şirket içi projesine ayarlamalısınız. Dağıtımlar yalnızca LCS ile başlatılabilir. LCS içinde şirket içi projeleri kurmak hakkında daha fazla bilgi için bkz [Lifecycle Services'ta bir şirket içi proje oluştur](../lifecycle-services/lbd-create-lcs-on-prem-project.md)

## <a name="authentication"></a>Kimlik Doğrulama

Şirket içi uygulaması AD FS ile çalışır. LCS ile etkileşim kurmak için, Azure Active Directory (Azure AD) de yapılandırmanız gerekir.

## <a name="standalone-service-fabric"></a>Tek başına Service Fabric

Finance and Operations, Tek başına Service Fabric kullanır. Daha fazla bilgi için bkz. [Service Fabric belgeleri](/azure/service-fabric/).

## <a name="infrastructure"></a>Altyapı

Finance and Operations bir hiper yakınsama mimarisinde çalışacak şekilde tasarlanmıştır. Donanım yapılandırması aşağıdaki bileşenleri içerir:

- Windows Server 2016 sanal makinelerine (VM'ler) dayalı Tek başına Service Fabric kümesi
- SQL Sunucu (Kümelenmiş SQL ve Her zaman açık desteklenir)
- Kimlik doğrulama için AD FS
- Sunucu Mesaj Bloğu (SMB) sürüm 3, depolama için dosya paylaşımı
- İsteğe bağlı: Microsoft Office Server 2017

Daha fazla bilgi için bkz [Sistemi gereksinimleri](../get-started/system-requirements.md) ve Boyutlandırma kılavuzları.

### <a name="hardware-layout"></a>Donanım düzeni

Alt yapı ve Service Fabric kümenizi, [Şirket içi ortamlar için donanım boyutlandırma](../get-started/hardware-sizing-on-premises-environments.md) dayalı olarak planlayın. Service Fabric kümesini planlamak hakkında daha fazla bilgi için bkz [Service Fabric tek başına küme dağıtımınızı planlama ve hazırlama](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Aşağıdaki tablo donanım düzenin örneğini gösterir. Bu örnek, bu konuda kurulumu göstermek için kullanılır.

> [!NOTE]
> Service Fabric kümesinin birincil düğümü en az üç düğüme sahip olmalıdır. Bu örnekte, **OrchestratorType** birincil düğüm türü olarak atanır.

| Makine amacı                                 | Makine adı    | IP adresi    |
|-------------------------------------------------|-----------------|---------------|
| Etki alanı denetleyicisi                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Dosya sunucusu                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Herzaman açık küme                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| İstemci                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric kümesi/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric kümesi/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric kümesi/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric kümesi/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric kümesi/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric kümesi/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric kümesi/Yönetim Raporlayıcı düğümü | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric kümesi/SSRS düğümü                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Kurulum

### <a name="prerequisites"></a>Ön koşullar

Kuruluma başlamadan önce aşağıdaki önkoşulların yerine getirilmiş olması gerekir. Bu kurulumun önkoşulları bu belgenin kapsamı dışındadır.

- Active Directory Domain Services (AD DS) yüklü ve ağınızda yapılandırılmış.
- AD FS dağıtıldı.
- SQL Server, SSRS ve Management Studio yüklüdür.

### <a name="overview"></a>Özet

Finance and Operations alt yapısının kurmak için aşağıdaki adımlar tamamlanmalıdır.

1. Etki alanı adınız ve DNS bölgelerinizi planlayın
2. Sertifikalarınız planlayın ve tedarik edin
3. Kullanıcılarınızı ve Hizmet hesaplarınızı planlayın
4. DNS bölgeleri oluşturun ve A kayıtları ekleyin
5. VM'leri Etki alanına katın
6. VM'lere önkoşul yazılım ekleyin
7. LCS'den kurulum komut dosyaları indirin
8. Yapılandırmanızı açıklayın
9. Sertifikaları yükleyin
10. Bir tek başına Service Fabric Kümesi ayarlayın
11. Kiracı için LCS bağlantısını yapılandırın
12. Dosya Depolama ayarlayın
13. SQL Sunucusu ayarlayın
14. Veritabanlarını yapılandırın
15. Kimlik bilgilerini şifreleyin
16. SSRS'u ayarla
17. AD FS'yi yapılandırın

### <a name="plan-your-domain-name-and-dns-zones"></a>Etki alanı adınız ve DNS bölgelerinizi planlayın

AOS yüklemeniz için halka açık kaydedilmiş bir etki alanı adını kullanmanızı öneririz. Bu şekilde, dışarıdan erişime gerek duyulursa ağın dışından erişilebilir.

Örneğin şirketinizin etki alanı contoso.com ise, Finance and Operations (şirket içi) bölgeniz d365ffo.onprem.contoso.com olabilir ve ana bilgisayar adları aşağıdaki gibi olabilir:

- AOS makineleri için ax.d365ffo.onprem.contoso.com
- Service Fabric kümesi için sf.d365ffo.onprem.contoso.com

### <a name="plan-and-acquire-your-certificates"></a>Sertifikalarınız planlayın ve tedarik edin

Service Fabric kümesinin ve dağıtılmış olan tüm uygulamaların güvenliğini sağlamak için Secure Sockets Layer (SSL) sertifikaları gereklidir. Üretim ve korumalı alan iş yükleriniz için [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), veya [GlobalSign](https://www.globalsign.com/en/ssl/) gibi bir sertifika yetkilisinden sertifikalar almanızı öneririz. Etki alanınız [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) ile ayarlanmışsa, sertifikaları AD CS ile oluşturabilirsiniz. her bir sertifikanın anahtar değişimi için oluşturulmuş bir özel anahtar içermesi gerekir ve Kişisel Bilgi Değişimi (.pfx) dosyasına dışa aktarılabilir olması gerekir.

Kendinden imzalı sertifikalar yalnızca test amaçlarıyla kullanılabilir. Kolaylık için kurulum komut dosyaları, kendinden imzalı sertifikalar oluşturmak ve dışa aktarmak için kurulum komut dosyaları içerir. Belirtmiş olduğumuz gibi, bu sertifikalar yalnızca test amaçlı kullanılmalıdır.

| Amaç                                      | Açıklama | Ek gereksinimler |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL sertifikası                   | Bu sertifika, ağ üzerinde bir SQL Server ve istemci uygulaması arasında aktarılan veriyi şifrelemek için kullanılır. | <p>Sertifikanın etki alanı adı, SQL Server örneğinin veya dinleyicisinin tam kalifiye etki alanı adı (FQDN) ile eşleşmelidir.</p><p>Örneğin, SQL dinleyicisi DAX7SQLAOSQLA makinesinde yer alıyorsa, sertifikanın DNS adı DAX7SQLAOSQLA.onprem.contoso.com olmalıdır.</p> |
| Service Fabric Server sertifikası            | Bu sertifika, Service Fabric düğümleri arasındaki düğümden düğüme iletişimi güvenli hale getirmek için kullanılır. Bu sertifika ayrıca kümeye bağlanan istemciye sunulan Sunucu sertifikası olarak da kullanılır. | <p>Sertifikanın etki alanı adının AOS ve Service Fabric'in barındırıldığı DNS bölgesi ile eşleşmesi gerekir.</p><p>Örneğin, sertifikanın etki alanı adı \*.onprem.contoso.com veya \*.contoso.com olabilir.</p><p>Bir joker karakter sertifikası kullanıyorsanız, joker karakteri yalnızca bir düzeye uygulanır. Bir alt etki alanı, özne alternatif adı (SAN), önceki örnekte örneğin \*.contoso.com gibi birden fazla düzey varsa, sertifikaya uygulanmalıdır.</p> |
| Service Fabric İstemci sertifikası            | Bu sertifika Service Fabric kümesini görüntüleyen ve yöneten istemciler tarafından kullanılır. | |
| Şİfreleme Sertifikası                     | Bu sertifika SQL Server şifresi ve kullanıcı hesabı parolaları gibi hassas bilgileri şifrelemek için kullanılır. | <p>Sertifika anahtarı kullanımı Veri Şifreleme (10) içermelidir ve Sunucu Kimlik Doğrulaması veya İstemci Kimlik Doğrulaması içermemelidir.</p><p>Daha fazla bilgi için bkz. [Service Fabric uygulamalarında gizliliği yönetmek](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL Sertifikası                          | <p>Bu sertifika ayrıca AOS web sitesi için istemciye sunulan Sunucu sertifikası olarak da kullanılır. Ayrıca Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) sertifikalarını etkinleştirmek için de kullanılır.</p><p>Service Fabric Server sertifikası bir joker sertifikası ise kullanılabilir.</p> | <p>Sertifikanın etki alanı adının AOS ve Service fabric'in barındırıldığı DNS bölgesi ile eşleşmesi gerekir.</p><p>Örneğin, sertifikanın etki alanı adı \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com, veya \*.contoso.com olabilir.</p><p>Bir joker karakter sertifikası kullanıyorsanız, joker karakter yalnızca bir düzeye uygulanır. Bir alt etki alanı, SAN, önceki örnekte örneğin \*.contoso.com gibi birden fazla düzey varsa, sertifikaya uygulanmalıdır.</p> |
| Oturum Kimlik doğrulama sertifikası           | Bu sertifika AOS tarafından bir kullanıcının oturum bilgilerini güvenli hale getirmek için kullanılır. | Bu ayrıca LCS'den dağıtım zamanında kullanılacak **Dosya Paylaşımı** Sertifikası'dır. |
| Veri Şifreleme ve Veri İmzalama sertifikası | Bu sertifikalar AOS tarafından önemli bilgileri şifrelemek için kullanılır. | |
| Mali Raporlama istemci sertifikası       | Bu sertifika, Mali Raporlama hizmetleri ve AOS arasındaki iletişimi güvenli hale getirmek için kullanılır. | |
| Raporlama Sertifikası                        | Bu sertifika, SSRS ve AOS arasındaki iletişimi güvenli hale getirmek için kullanılır. | |
| Şirket içi yerel aracı sertifikası           | <p>Bu sertifika, şirket içinde barındırılan bir yerel aracı ve LCS arasındaki iletişimi güvenli hale getirmeye yardımcı olmakta kullanılır.</p><p>Bu sertifika, yerel aracıyı sizin adınıza Azure AD kiracınızda hareket etmek, LCS ile iletişim kurmak ve dağıtımları izlemek üzere etkin hale getirir.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Kullanıcılarınızı ve hizmet hesaplarınızı planlayın

Finance and Operations (şirket içi) çalışması için çeşitli kullanıcı ve hizmet hesapları oluşturmanız gerekir. Grup yönetilen hizmet hesapları (gMSAs), etki alanı hesapları ve SQL hesapları arasında bir kombinasyon oluşturmanız gerekir. Aşağıdaki bu örnekte kullanılacak tablo kullanıcı hesaplarını, amaçlarını ve örnek adlarını gösterir.

| Kullanıcı hesabı                                            | Türü           | Amaç | Kullanıcı adı |
|---------------------------------------------------------|----------------|---------|-----------|
| Mali Raporlama Uygulama Hizmet Hesabı         | gMSA           |         | Contoso\\svc-FRAS$ |
| Mali Raporlama İşlem Hizmet Hesabı             | gMSA           |         | Contoso\\svc-FRPS$ |
| Mali Raporlama Tek Tıkla Tasarımcı Hizmet Hesabı | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS Hizmet Hesabı                                     | gMSA           | Bu kullanıcı, geleceğe hazırlık için oluşturulmalıdır. Gelecek sürümlerde AOS ile gMSA'nın birlikte çalışmasını planlıyoruz. Bu kullanıcıyı kurulum zamanında oluşturarak, gMSA'ya sorunsuz geçiş garanti etmeye yardımcı olursunuz. | Contoso\\svc-AXSF$ |
| AOS Hizmet Hesabı                                     | Etki alanı hesabı | AOS bu kullanıcıyı GA sürümünde kullanır. | Contoso\\AXServiceUser |
| AOS SQL DB Yönetici kullanıcsı                                   | SQL kullanıcısı       | Finance and Opertions bu kullanıcıyı SQL ile kimlik doğrulaması için kullanır\*. Bu kullanıcı gelecekteki sürümlerde gMSA kullanıcısı ile değiştirilecektir. | AXDBAdmin |
| Yerel Dağıtım Aracısı Hizmet Hesabı                  | gMSA           | Bu hesap yerel aracı tarafından çeşitli düğümlerdeki gelişimi yönetmek için kullanılır. | Contoso\\Svc-LocalAgent$ |

\* SQL kimlik doğrulama için SQL kullanıcı adı ve parolası güvenlidir çünkü şifrelenmişlerdir ve dosya paylaşımında depolanmışlardır.

### <a name="create-dns-zones-and-add-a-records"></a>DNS bölgeleri oluşturun ve A kayıtları ekleyin

DNS AD DS ile tümleşiktir ve bir ağdaki kaynakları organize etmenize, yönetmenize ve bulmanıza olanak sağlar. AOS ana bilgisayar adı ve Service Fabric kümesi için bir DNS yönlendirme arama bölgesi ve A kayıtları oluşturun. Bu örnek kurulumda DNS bölge adı d365ffo.onprem.contoso.com'dur ve A kayıtları/ana bilgisayar adları aşağıdaki gibidir:

- AOS makineleri için **ax**.d365ffo.onprem.contoso.com
- Service Fabric kümesi için **sf**.d365ffo.onprem.contoso.com

#### <a name="add-a-dns-zone"></a>DNS bölgesi ekle

Bir DNS bölgesi eklemek için aşağıdaki yordamı kullanın.

1. Etki alanı denetleyici makineye oturum açın, **Başlat**'ı tıklatın ve **dnsmgmt.msc** yazarak DNS Yöneticisini başlatın.
2. Etki alanı denetleyici adına sağ tıklayın ve sonra **Yeni Bölge** \> **İleri**'yi seçin.
3. **Birincil Bölge**'yi seçin.
4. **Bölgeyi Active Directory'de depola (yalnızca DNS Sunucusu yazılabilir bir etki alanı denetleyicisiyse kullanılabilir)** onay kutusunu seçili bırakın ve **İleri**'yi tıklatın.
5. **Bu etki alanı içindeki Etki Alana Denetleyicileri üzerinde çalışan tüm DNS Sunucularına: Contoso.com** seçimini belirleyin ve sonra **İleri**'yi tıklatın.
6. **İleriye Doğru Arama Bölgesi**'ni seçin ve sonra **İleri**'yi tıklatın.
7. Kurulumunuz için bölge adını girin ve ardından **İleri**'yi tıklatın. Örneğin **d365ffo.onprem.contoso.com** girin.
8. **Dinamik güncelleştirmelere izin verme**'yi seçin ve **İleri**'yi tıklatın.

#### <a name="set-up-an-a-record-for-aos"></a>AOS için bir A kaydı ayarlayın

Yeni DNS bölgesinde, **AOSNodeType** türündeki **her bir** Service Fabric küme düğümü için **ax.d365ffo.onprem.contoso.com** adındaki bir A kaydı oluşturun. Diğer düğüm türleri için A kayıtları oluşturmayın.

1. Yeni bölgeye sağ tıklayın ve sonra **Yeni Ana Bilgisayar**'ı tıklatın.
2. Service Fabric düğümünün adını ve IP adresini girin (ör. 10.179.108.12), ve sonra **Ana Bilgisayar Ekle**'yi tıklatın.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Düzenleyici için bir A Kaydı ayarlayın

Yeni DNS bölgesinde, **OrchestratorType** türündeki **her bir** Service Fabric küme düğümü için **sf.d365ffo.onprem.contoso.com** adındaki bir A kaydı oluşturun. Diğer düğüm türleri için A kayıtları oluşturmayın.

1. Yeni bölgeye sağ tıklayın ve sonra **Yeni Ana Bilgisayar**'ı tıklatın.
2. Service Fabric düğümünün adını ve IP adresini girin (ör. 10.179.108.15), ve sonra **Ana Bilgisayar Ekle**'yi tıklatın.

#### <a name="join-vms-to-the-domain"></a>VM'leri etki alanına katın

[Windows Server 2016'yı bir Active Directory etki alanına katmak](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) içerisindeki adımları tamamlayarak her bir VM'i etki alanına katın. Alternatif olarak Windows PowerShell komut dosyasını kullanın.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
VM'ler etki alanına katıldıktan sonra, AOS Hizmet Hesapları'nı (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) yerel yönetici grubuna ekleyin. Bunu nasıl yapıldığını görmek için [Yerel gruba bir üye ekle](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) makalesine göz atın.

#### <a name="disable-user-access-control"></a>Kullanıcı Erişim Denetimi'ni devre dışı bırak 

Kullanıcı Erişim Denetimi'ni **tüm** Service Fabric düğümlerinde devre dışı bırakmak için aşağıdaki komut dosyasını çalıştırın.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Komut başarıyla tamamlandıktan sonra düğümü yeniden başlatmalısınız.

#### <a name="add-prerequisite-software-to-vms"></a>VM'lere önkoşul yazılım ekleyin

Aşağıdaki tablo her bir düğüm türündeki makinelere uygulanması gereken önkoşul yazılımı listeler.

> [!NOTE]
> Bileşenleri yeniden başlattıktan sonra bilgisayarınızı yeniden başlatmanız gerekir.

| Düğüm türü | Bileşen | Komut |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC sürücüsü | Bkz: [SQL Server için Microsoft ODBC Sürücüsü 13.1 - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework sürümü 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework sürümü 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet Information Services (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual Studio 2013 için Microsoft Visual C++ Yeniden Dağıtılabilir Paketleri | Bkz. [Microsoft Visual Studio 2013 için Microsoft Visual C++ Yeniden Dağıtılabilir Paketleri](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Yeniden Dağıtılabilir | Bkz. [Microsoft Access Database Engine 2010 Yeniden Dağıtılabilir](https://www.microsoft.com/en-us/download/details.aspx?id=13255). |
| BI        | .NET Framework sürümü 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework sürümü 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | **Yerel** modda SQL Server Raporlama Servisleri 2016 | |
| MR        | .NET Framework sürümü 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework sürümü 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual Studio 2013 için Microsoft Visual C++ Yeniden Dağıtılabilir Paketleri | Bkz. [Microsoft Visual Studio 2013 için Microsoft Visual C++ Yeniden Dağıtılabilir Paketleri](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>LCS'den kurulum komut dosyaları indirin

Bu kurulum deneyimini geliştirmek için çeşitli komut dosyaları sağladık. Kurulum komut dosyalarını LCS'den indirmek için bu adımları izleyin.

1. LCS'ye oturum açın (<https://lcs.dynamics.com/v2>).
2. Panoda **Paylaşılan varlık kütüphanesi** dosyasına tıklayın.
3. **Model** sekmesini tıklatın.
4. Kılavuzda **Microsoft Dynamics 365 for Operations - Şirket içi Dağıtım komut dosyaları** satırını seçin.
5. **Sürümler**'i tıklatın ve komut dosyalarının en son sürümünü indirin.

### <a name="describe-your-configuration"></a>Yapılandırmanızı açıklayın

Bu bölüm çalıştırmanız gereken komut dosyaları hakkında bilgi sağlar. Komut dosyaları çalıştırmanız gereken sırada ele alınmaktadır. Komut dosyalarını çalıştırmak için $(downloadPath)\\ConfigTemplate.xml şablon dosyasını doldurun. ConfigTemplate.xml dosyası Service Fabric kümelerini, bunların yapılandırılmasında kullanılan sertifikaları ve ilgili sertifikalara erişim izni verilmesi gereken hesapları açıklar. Sağlanmış olan örnekte, değerler bu başlıkta açıklanan örnek altyapı için doldurulmuştur. Şablon dosyası bir sonraki bölümde kullanılır.

#### <a name="create-the-domain-account-for-a-service-user"></a>Bir hizmet kullanıcısı için etki alanı hesabı oluştur

Aşağıdaki komutu contoso\\AXServiceUser etki alanı kullanıcısı hesabını oluşturmak için çalıştırın.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSAs oluştur

1. Dizini **$(DownloadPath)** olarak değiştirin ve aşağıdaki Windows PowerShell komutunu çalıştırın.

    > [!NOTE]
    > Bu komut kullanıcıları oluşturmaz. Bunun yerine etki alanı denetleyici makinede el ile çalıştırılması gereken komutları yazdırır.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Komutun çıktısını Windows PowerShell penceresine kopyalayın. Satır sonlarının kaldırıldığından emin olun ve satırları Active Directory etki alanı denetleyici makinede, yükseltilmiş yetkilerle çalıştırın (sağ tıkla ve **Yönetici olarak çalıştır** üzerine tıklayın).
3. Hesapların başarıyla oluşturulduğunu doğrulamak için aşağıdaki komut dosyasını Active Directory etki alanı denetleyici makinenin üzerinde çalıştırın. Komutu, deseni hizmet hesaplarının adlandırma kuralıyla eşleştirecek şekilde değiştirdiğinizden emin olduktan sonra çalıştırın.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Export-AddGMSAsONVMScript.ps1 komut dosyasını istemci makinede çalıştırın. Bu komut dosyası, her bir Service Fabric VM üzerinde çalıştırılan komut dosyalarını oluşturur ve onları her bir VM adına karşılık gelen klasörlere ekler.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS'i Durdur

Her bir Service Fabric VM'e bağlanmak için Uzaktan Masaüstü Protokolünü (RDP) kullanın ve [Web Sunucusunu Başlat veya Durdur (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) içerisindeki el ile gerçekleştirilecek işlemleri tamamlayın. Alternatif olarak her bir Service Fabric VM'e bağlanmak için RDP kullanarak aşağıdaki Windows PowerShell komut dosyasını çalıştırın.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_Ürün içerisindeki IIS dll'leri ile bazı bağımlılıklar olduğu için IIS özelliği yüklenmelidir ancak devre dışı bırakılmalıdır._

### <a name="install-certificates"></a>Sertifikaları yükleyin

1. Bu başlıkta daha önce listelenen sertifikaları geçerli bir CA'dan satın aldıysanız, .pfx dosyası adını ve sertifikalar için parmak izini ConfigTemplate.xml dosyasında doldurun. **generateSelfSignedCert** özniteliğini **Yanlış** ve **dışa aktarılabilir** özniteliğini **Yanlış** olarak ayarlayın. .pfx dosyalarını $(DownloadPath)\\InfrastructureScripts\\Certs klasörüne kopyalayın.
2. Otomatik olarak imzalanan sertifikalar kullanıyorsanız (yalnızca test amacıyla), aşağıdaki komut dosyasını çalıştırın. Otomatik olarak imzalanan sertifikalar oluşturmak için ConfigTemplate.xml dosyasında, **generateSelfSignedCert** ayarının **Doğru** ve **Dışa aktarılabilir** ayarının **Doğru** olarak ayarlandığından emin olun. Komut dosyası XML'i sertifikalar için parmak iziyle güncelleştirir.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Yeni sertifikaları özel anahtar ile dışa aktarın (.pfx dosyası). Dışa aktarma komutlarını Windows PowerShell'de oluşturmak ve çalıştırmak için aşağıdaki komut dosyasını kullanın. .pfx dosyaları Certs klasörüne koyulacaktır.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Sertifikaların yüklemiş olması ve sertifika içinde mevcut olması gerekir:\\CurrentUser\\My. Sertifikalar dışa aktarılabilir de olması gerekir.

    Otomatik olarak imzalanan sertifikalar kullanıyorsanız, sonraki bölüme atlayın. Bu yordamı tamamlamanız gerekmez.

4. .pfx dosyalarını $(DownloadPath)\\InfrastructureScripts\\Certs klasörüne dışa aktardıktan veya kopyaladıktan sonra VM'lere karşılık gelen klasörlere koyulacak komut dosyalarını oluşturmak için aşağıdaki komutları çalıştırın.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Her bir klasördeki komut dosyalarını, klasör adına karşılık gelen VM'lere kopyalayın.
6. Her bir VM içerisinde, aşağıdaki komut dosyalarını göründükleri sırada çalıştırın.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Bir tek başına Service Fabric kümesi ayarlayın

1. ClusterConfig.json dosyası oluşturmak için aşağıdaki komutu çalıştırın.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Daha fazla bilgi için bkz., [Adım 1B: Bir çoklu makine kümesi oluştur](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Windows üzerinde X.509 sertifikaları kullanarak bir tek başına kümeyi güvenli hale getir](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security), ve [Windows Server üzerinde çalışan bir tek başına küme oluştur](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. [Service Fabric tek başına yükleme paketi](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package)'ni indirin. Zip dosyası karşıdan yüklendikten sonra zip dosyası sağ tıklayıp **Özellikler**'e tıkladıktan sonra bloke durumunu kaldırın. İletişim kutusunda sağ altta **Engellemeyi Kaldır** onay kutusunun seçin.
3. Zip dosyasını Service Fabric kümesindeki düğümlerden birine kopyalayın ve sıkıştırmasını açın.
4. Gelen güvenlik duvarı kuralını tüm düğümlerde bağlantı noktaları 443 ve 445'te oluşturmak için aşağıdaki komutları çalıştırın.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Gelen güvenlik duvarı kuralını sadece SSRS düğümünde bağlantı noktası 80'de oluşturmak için aşağıdaki komutları çalıştırın.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. ClusterConfig.json dosyanızı, sıkıştırması açılmış tek başına Service Fabric kurulum konumunuza kopyalayın.
7. Windows PowerShell'de artırılmış izinler kullanarak sıkıştırması açılmış kurulum konumunuza gidin ve ClusterConfig'inizi test etmek için aşağıdaki komutu çalıştırın.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Test başarılı olursa, kümeyi dağıtmak için aşağıdaki komutu çalıştırın.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Küme oluşturulduktan sonra, Service Fabric gezginini herhangi bir istemci makinede kurulumu doğrulamak için açın:

    1. Service Fabric istemci sertifikasını, zaten yüklü değilse CurrentUser\\My konumuna yükleyin.
    2. **IE ayarları** \> **Uyumluluk Modu**'na gidin ve **Intranet sitelerini uyumluluk modunda görüntüle** onay kutusunu temizleyin.
    3. sf.d365ffo.onprem.contoso.com'un bölgede belirtilen Service Fabric kümesinin ana bilgisayar adı olduğu `https://sf.d365ffo.onprem.contoso.com:19080` üzerine gidin. DNS adı çözümleme yapılandırılmamışsa, makinenin IP adresini kullanın.
    4. İstemci sertifikasını seçin. **Service Fabric gezgini** sayfası açılır.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Kiracı için LCS bağlantısını yapılandırın

Finance and Operations dağıtım ve bakımı, LCS aracılığıyla şirket içi yerel aracı kullanılarak düzenlenebilir. LCS'den Finance and Operations kiracısına bağlantı kurmak için, önce Azure AD kiracınız adına hareket edecek yerel aracıyı etkinleştiren sertifikayı yapılandırmanız gerekir (örneğin Contoso.Onmicrosoft.com).

Bir CA'dan alınan veya komut dosyalarını kullanarak oluşturduğunuz otomatik olarak imzalanan şirket içi aracı sertifikasını kullanarak.

Yalnızca Genel Yönetici dizin rolüne sahip hesaplar LCS'ye yetki vermek için sertifikalara ekleyebilir. Varsayılan olarak, kuruluşunuz için Microsoft Office 365 için kaydolan kişi, dizinin genel yöneticisi olacaktır.

> [!NOTE]
> Sertifikayı kiracı başına tam olarak bir defa yapılandırmanız gerekir. Tüm şirket içi ortamlar LCS'ye bağlanmak için aynı sertifikayı kullanabilir.

1. Azure PowerShell'in en son sürümünü bir istemci makineye indirin ve yükleyin. Daha fazla bilgi için bkz [Azure PowerShell indirin ve yükleyin](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Genel Yönetici dizin rolüne sahip olduğunuzu doğrulamak için [Müşterinin Azure portalı](https://portal.azure.com)'na oturum açın.
3. Aşağıdaki komut dosyasını $(DownloadPath)\\InfrastructureScripts üzerinden çalıştırın.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Dosya depolamayı ayarlayın

İki adet yüksek oranda kullanılabilr SMB 3.0 dosya paylaşımı ayarlamanız gerekir. SMB 3.0'ı etkinleştirmek hakkında daha fazla bilgi için bkz.[SMB Güvenlik Geliştirmeleri](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Güvenli lehçe anlaşma SMB 2.0 veya 3.0'dan SMB 1.0'a indirgemeleri algılayamaz veya engelleyemez. Bu sebeple ve SMB şifrelemenin tam kabiliyetlerini kullanabilmek için SMB 1.0 sunucusunu devre dışı bırakmanızı öneririz.

> [!NOTE]
> Ortamınızda barındırılırken verinizin korunduğunu garanti etmeye yardımcı olmak için BitLocker Sürücü Şifreleme'nin her cihaz üzerinde etkinleştirilmiş olması gerekir. BitLocker'ı etkinleştirmek hakkında daha fazla bilgi için bkz. [BitLocker: Windows Server 2012 ve sonrasında nasıl etkinleştirilir](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- AOS'ye yüklenen kullanıcı belgelerini depolayan bir dosya paylaşımı (örneğin, \\\\DAX7SQLAOFILE1\\aos-storage).
- Dağıtımı düzenlemek için en son oluşturma ve yapılandırma dosyalarını depolayan bir dosya paylaşımı (örneğin, \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Paylaşıma koyulacak dosyalarda yol uzunluğunu aşmayı engellemek için bu dosya yolunu mümkün olduğunca kısa tutun.

1. Dosya paylaşımı makinesinde aşağıdaki komutu çalıştırın.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>\\\\DAX7SQLAOFILE1\\aos-storage dosya paylaşımını ayarlayın

2. Sunucu Yöneticisi'nde **Dosya ve Depolama Hizmetleri** \> **Paylaşımlar**'ı seçin.
3. **aos-storage** adına sahip yeni bir paylaşım oluşturmak için **Görevler** \> **Yeni Paylaşım** üzerine tıklayın.
4. Service Fabric kümesindeki **OrchestratorNodeType** hariç her makine için **Değiştirme** izinleri verin.
5. AOS etki alanı kullanıcısı (contoso\\AXServiceUser) ve gMSA kullanıcısı (contoso\\svc-AXSF) için **Değiştirme** izinleri verin.

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>\\\\DAX7SQLAOFILE1\\agent dosya paylaşımını ayarlayın

6. Sunucu Yöneticisi'ne geri gidin, **Dosya ve Depolama Hizmetleri** \> **Paylaşımlar**'ı seçin.
7. **agent** adına sahip yeni bir paylaşım oluşturmak için **Görevler** \> **Yeni Paylaşım** üzerine tıklayın.
8. Yerel dağıtım aracısı (contoso\\svc-LocalAgent$) için **Tam-Denetim** izinleri verin.

### <a name="set-up-sql-server"></a>SQL Sunucusu ayarlayın

1. Yüksek kullanılabilirlik ile SQL Server 2016 SP1'i Storage Area Network (SAN) veya Her zaman açık yapılandırması olarak yükleyin.  **Veritabanı Altyapısı, Raporlama Hizmetleri, Tam Metin Arama** ve **Yönetim Araçları**'nın zaten yüklenmiş olduğunu doğrulayın.
> [!NOTE]
> SQL Her zaman açık'ın [İlk Veri Eşitleme Sayfası'nı seç (Her Zaman Açık Grup Sihirbazları)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards)'na uygun olarak kurulmuş olduğundan emin olun ve [İkincil Veritabanlarını El İle Hazırlamak için](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)'i takip edin
2. SQL Service'i bir etki alanı kullanıcısı olarak çalıştırın.
3. Finance and Operations'u yapılandırmak için bir CA'dan bir SSL sertifikası alın. Test amaçlı olarak otomatik olarak imzalanmış sertifikalar oluşturabilir ve kullanabilirsiniz.

**Otomatik olarak imzalanmış Kümelenmiş SQL örneği**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Otomatik olarak imzalanmış Her Zaman Açık SQL örneği**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Sertifikayı kullanarak [Microsoft Management Console kullanarak bir SQL Sunucusu'nun bir örneği için SSL şifrelemeyi etkinleştirmek](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) içindeki adımları tamamlayın.
5. Kümedeki her bir düğüm için aşağıdaki adımları izleyin. Değişiklikleri etkin olmayan düğümde yaptığınızdan emin olun ve değişiklikler yapıldıktan sonra ona devredin.

    1. Sertifikayı LocalMachine\\My üzerine içe aktarın.
    2. SQL hizmetini çalıştırmak için kullanılan hizmet hesabına sertifika izinleri verin. Microsoft Management Console'da (MMC), sertifika (certlm.msc) üzerine sağ tıklayın ve sonra **Görevler** \> **Özel Anahtarları Yönet** üzerine tıklayın.
    3. Sertifika parmak içini HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate üzerine ekleyin.
    4. Microsoft SQL Yapılandırma Yöneticisi'nde **ForceEncryption**'ı **Evet** olarak ayarlayın.

6. Sertifikanın ortak anahtarını (.cer dosyasını) dışa aktarın ve her bir Service Fabric düğümünün güvenilir kök dizinine yükleyin.

### <a name="configure-the-orchestratordata-database"></a>OrchestratorData veritabanını yapılandırın

1.  Boş bir veritabanı oluşturun, **OrchestratorData** olarak adlandırın. Bu veritabanı, şirket içi aracı tarafından dağıtımları yönetmek için kullanılır.
2.  Yerel aracıya veritabanı üzerinde gMSA (svc-LocalAgent$) **db\_sahip** izinlerini verin:

    1. Ağaçta, sunucu adını genişletin, **Güvenlik** \> **Oturumlar**'ı genişletin, daha sonra sağ tıklayın ve **Yeni Oturum açma**'yı tıklatın.

        ![Yeni Oturum açma komutu](./media/OPSetup_01_NewLogin.png)


    2. **svc-LocalAgent$** hizmet hesabını arayın. **Konumlar**'ı tıklatın ve **Tüm Dizin**'i seçin, sonra **Nesne Türleri**'ni tıklatın ve **Hizmet Hesabı**'nı seçin.

        ![Kullanıcıyı, Servis Hesabını veya Grup iletişim kutusunu seçin](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. **ServerRole Ata**'yı **Ortak** olarak ayarlayın.
    4. **db\_sahip** veritabanı rolünü OrchestratorData veritabanına atayın.

### <a name="configure-the-finance-and-operations-database"></a>Finance and Operations veritabanını yapılandırın

1. LCS'ye oturum açın (<https://lcs.dynamics.com/v2>).
2. Panoda **Paylaşılan varlık kütüphanesi** dosyasına tıklayın.
3. **Model** sekmesini tıklatın 
4. Izgarada, **Dynamics 365 for Operations on-premises, Enterprise edition - Demo verisi** satırını zip'i indirek için tıklayın.
5. Zip, boş ve demo verisi .bak dosyalarını içerir. İhtiyaçlarınıza uygun olarak uygun .bak dosyasını seçin. Örneğin, demo verileri gerekiyorsa, AxBootstrapDB_Demodata.bak dosyasını geri yükleyin. 
6. AxBootstrapDB_DemoData.bak veritabanını geri yükleyin.
7. Veritabanı **AXDBRAIN** olarak yeniden adlandırın.
8. Geri yüklenen veri tabanında aşağıdaki sorguları çalıştırın.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Veritabanı dosyalarını karşıya güncelleştirin:

    1. Veritabanını sağ tıklayın ve sonra **Özellikler**'i tıklatın
    2. Veritabanı dosya özelliklerini değiştirmek için **Dosyalar**'ı tıklatın.
    3. **Başlangıç Boyutu (MB)** alanında, 5.120'den büyük bir değer girin.

        ![Veritabanı Özellikleri iletişim kutusu](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. **AXDBBuild\_Data** için **Autogrowth/Maximize** alanını **200** megabayt (MB) olarak ayarlayın.
    5. **AXDBBuild\_Log** için **Autogrowth/Maximize** alanını **500** MB olarak ayarlayın.

        ![Autogrowth iletişim kutusunu değiştirin](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. SQL kimlik doğrulaması (axdbadmin) etkinleştirilmiş yeni bir kullanıcı oluşturun.
6. Kullanıcıları ve veritabanı rollerini eşleştirmek için aşağıdaki tablodaki bilgileri kullanın.

    | Kullanıcı             | Türü    | Veritabanı rolü |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. svc-AXSF$ kullanıcısı ve axdbadmin SQL kullanıcısına tempdb veritabanında aşağıdaki kurallara erişim verin:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Management Studio'da aşağıdaki Transact SQL (T-SQL) komutlarını çalıştırın:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Aşağıdaki komutu çalıştırın:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Mali Raporlama veritabanını yapılandırın

1.  Boş bir veritabanı oluşturun, **FinancialReporting** olarak adlandırın.
2.  Kullanıcıları ve veritabanı rollerini eşleştirmek için aşağıdaki tablodaki bilgileri kullanın.

    | Kullanıcı             | Türü | Veritabanı rolü |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Kimlik bilgilerini şifreleyin

1. Herhangi bir istemci makinesinde LocalMachine\\Sertifika depolamam içerisindeki şifreleme sertifikasını yükleyin.
2. Geçerli kullanıcıya bu sertifikanın özel anahtarını okuma izni verin.
3. Aşağıda gösterildiği gibi Credentials.json dosyası oluşturun.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword**, AOS etki alanı kullanıcısı (contoso\\axserviceuser) için şifrelenmiş etki alanı parolasıdır.
    - **SqlUser**, Finance and Operations veritabanına (AXDBRAIN) erişimi olan şifrelenmiş SQL kullanıcısıdır (axdbadmin) ve **SqlPassword** şifrelenmiş SQL parolasıdır.

4. .json dosyasını SMB dosya paylaşımına kopyalayın, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Credentials.json dosyası şifreli verilerle güncelleştirin.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Credentials.json'da **\<encryptedDomainUserPassword\>** değerini şifreli etki alanı parolasıyla değiştirin.
    2. **\<encryptedSqlUser\>** değerini şifrelenmiş Finance and Operations SQL kullanıcısıyla değiştirin.
    3. **\<encryptedSqlPassword\>** değerini Finance and Operations SQL parolası ile değiştirin.
    
### <a name="set-up-ssrs"></a>SSRS'u ayarla

1.  Başlamadan önce, bu konunun başındaki önkoşulların yüklü olduğundan emin olun.
2.  [Şirket içi bir dağıtım için SQL Server Reporting Services'ı konfigüre etme](../analytics/configure-ssrs-on-premises.md) için adımları izleyin.

### <a name="configure-ad-fs"></a>AD FS'yi yapılandırın

Bu yordamı tamamlayabilmeniz için önce AD FS'nin Windows Server 2016'da dağıtılması gerekir. AD FS'yi dağıtmak hakkında daha fazla bilgi için bkz [Dağıtım Kılavuzu Windows Server 2016 ve 2012 R2 AD FS Dağıtım Kılavuzu](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations, AD FS varsayılan yapılandırmasına sistemde bulunmayan ek yapılandırmaya ihtiyaç duyar. Aşağıdaki adımlar için Windows PowerShell, AD FS rolü hizmetinin yüklü olduğu bir makinede çalışır. Bu kullanıcı AD FS'yi yönetmek için yeterli izinler sahip olmalıdır. Örneğin, kullanıcı bir etki alanı yönetici hesabına sahip olmalıdır.

1. AD FS kimlik tanımlayıcıyı, AD FS belirteç verici ile eşleşecek şekilde yapılandırın.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Intranet kimlik doğrulama bağlantıları için AD FS'yi karma ortamlar için yapılandırmadıysanız Windows Tümleşik Kimlik Doğrulama'yı (WIA) devre dışı bırakmalısınız. WIA'nın AD FS ile birlikte kullanılabilmesi için nasıl yapılandıracağınız hakkında daha fazla bilgi için bkz. [Tarayıcıları AD FS ile Windows Tümleşik Kimlik Doğrulama (WIA) kullanmak için yapılandır](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Oturum açma için, kullanıcının e-posta adresi kabul edilebilir bir kimlik doğrulama girişi olmalıdır.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

AD FS'nin kimlik doğrulaması değişimi için Finance and Operations'a güvenmesi için çeşitli uygulama girişlerinin AD FS içinde bir AD FS uygulama grubu altında kayıtlı olması gerekir. Kurulum işlemini hızlandırmak ve hataları azaltmaya yardımcı olmak için aşağıdaki komut dosyasını kayıt için kullanabilirsiniz. Publish-ADFSApplicationGroup.ps1 komut dosyasını ve D365FO-OP dizinini AD FS rolü hizmetinin yüklü olduğu bir makineye kopyalayın. Daha sonra komut dosyasını, örneğin bir yönetici hesabı gibi, AD FS'Yi yönetmek için yeterli izne sahip bir kullanıcı hesabı kullanarak çalıştırın. Komut dosyası kullanma hakkında daha fazla bilgi için komut dosyasında listelenen belgelere bakın. Çıkışta belirtilen İstemci kodu'nu not edin çünkü bu bilgi size LCS'de daha sonraki bir adımda sorulacaktır.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS yönetim konsolu aşağıdaki görsele benzer olmalıdır. Sunucu Yöneticisi'ni açın, **Araçlar** \> **AD FS Yönetimi** üzerine tıklayın ve daha sonra ağaç görünümünün altında solda, **Uygulama Grupları** üzerine tıklayın. Daha fazla ayrıntı görüntülemek için uygulama grubuna çift tıklayın.

![Uygulama grubu özellikleri](./media/OPSetup_05_ApplicatioGroupProperties.png)

Son olarak, sağlamlık denetimi için AD FS OpenID Yapılandırma URL'sine **AOSNodeType** türündeki bir Service Fabric düğümünden erişebildiğinizi, bir web tarayıcısında `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` adresine giderek doğrulayın. Sitenin güvenli olmadığına dair bir mesaj alırsanız, Trusted Root Certification Authorities depolamasına AD FS SSL sertifikasını eklememişsinizdir. Bu adım AD FS dağıtım kılavuzunda açıklanır. URL'ye başarıyla erişebilirseniz, AD FS yapılandırmanızı içeren bir JavaScript Object Notation (JSON) dosyası döndürülür ve AD FS URL'nizin güvenli olduğunu görürsünüz.

Bununla birlikte altyapı kurulumu tamamlanır. Aşağıdaki bölümler [LCS](https://lcs.dynamics.com)'ye bağlayıcınızı kurmak için nasıl gidebileceğinizi ve Dynamics 365 for Finance and Operations ortamınızı nasıl dağıtacağınızı açıklar.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Bağlayıcıyı yapılandırın ve şirket içi yerel aracıyı yükleyin

1. [LCS](https://lcs.dynamics.com/)'ye oturum açın ve şirket içi uygulama projesini açın.
2. Hamburger menüsünde **Proje ayarları**'nı tıklayın.

    ![Proje sunucu komutu](./media/OPSetup_06_ProjectSettings.png)

3. **On-premises bağlayıcılar**'ı tıklatın.
4. Yeni bir bağlayıcı oluşturmak için **Ekle**'ye tıklayın.
5. **Ana bilgisayar altyapı kurulumu** sekmesinde, aracı yükleyiciyi indirin.

    ![Kurulum ana bilgisayar altyapı sekmesindeki aracı yükleme indirme düğmesi](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Zip dosyasının engelinin kaldırıldığını doğrulayın. Dosyaya sağ tıklayın, **Özellikler** üzerine tıklayın ve **Engellemeyi kaldır**'ı seçin.
7. **OrchestratorType** türünün bir Service fabric düğümünde aracı yükleyicinin sıkıştırmasını açın.
8. **Aracıyı yapılandırma** sekmesinde, yapılandırma ayrıntılarını girin.
9. Yapılandırmayı kaydedin ve daha sonra **Yapılandırmaları indir** üzerine tıklayarak localagent-config.json yapılandırma dosyasını indirin.

    ![Aracı yapılandırma sekmesindeki Yapılandırmaları indir düğmesi](./media/OPSetup_08_DownloadConfigurations.png)

10. localagent-config.json dosyasını, aracı yükleme paketinin bulunduğu makineye kopyalayın.
11. Bir Komut İstemi penceresinde, aracı yükleyiciyi barından klasöre giderek aşağıdaki komutu çalıştırın.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Bu komutu çalıştan kullanıcının OrchestratorData veritabanları üzerinde **db\_owner** izinlerine sahip olması gerekir.
    
12. Yerel aracı başarıyla yüklendikten sonra, LCS'deki şirket içi bağlayıcınıza geri gidin.
13. **Kurulumu doğrula** sekmesinde, **İleti aracısı** düğmesini tıklatın. Bu, LCS'nin yerel aracınıza bağlantısını test edecektir. Bağlantı başarıyla oluşturulduğunda, sayfa aşağıdaki grafik gibi görünecektir.

     ![Aracıyı doğrula](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Dynamics 365 for Finance and Operations (şirket içi) ortamınızı dağıtın

1. LCS'de şirket içi projenize gidin, **Ortam**, **Korumalı alan** üzerine gidin ve **Yapılandır**'ı tıklatın.
2. **Ortam topolojisi**'ni seçin ve dağıtımınızı başlatmak için sihirbaza gidin.
3. Yerel aracı dağıtım isteğini alacaktır, dağıtımı başlatacaktır ve hazır olduğunda LCS ile iletişim kuracaktır.

