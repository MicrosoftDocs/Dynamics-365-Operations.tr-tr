---
title: Örnek kopyala
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010816"
---
# <a name="copy-an-instance"></a>Örnek kopyala

Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz. Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz.

Bir örneği kopyalamak için, aşağıdakileri yapmanız gerekir:

- Üzerine yazmak istediğiniz İnsan Kaynakları örneği bir korumalı alan ortamı olmalıdır.

- Kopyalama kaynağı ve hedef ortamlar aynı bölgede olmalıdır. Bölgeler arasında kopyalama yapamazsınız.

- Örneği kopyaladıktan sonra oturum açmak için hedef ortamda bir yönetici olmanız gerekir.

- İnsan Kaynakları veritabanını kopyaladığınızda, bir Microsoft PowerApps ortamda bulunan öğeleri (uygulamalar veya veriler) kopyalamayın. Bir PowerApps ortamdaki öğelerin nasıl kopyalanacağı hakkında bilgi için, bkz. [Ortam kopyalama](https://docs.microsoft.com/power-platform/admin/copy-environment). Üzerine yazmak istediğiniz PowerApps ortamı bir korumalı alan ortamı olmalıdır. PowerApps üretim ortamını korumalı alan ortamına dönüştürmek için genel bir kiracı yöneticisi olmanız gerekir. PowerApps ortamın değiştirilmesi hakkında daha fazla bilgi için, bkz. [Örneği değiştirme](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>İnsan Kaynakları veritabanını kopyalama etkileri

Bir İnsan Kaynakları veritabanını kopyaladığınızda aşağıdaki olaylar oluşur:

- Kopyalama işlemi hedef ortamdaki varolan veritabanını siler. Kopyalama işlemi tamamlandıktan sonra, varolan veritabanını kurtaramazsınız.

- Kopyalama işlemi tamamlanana kadar hedef ortam kullanılamayacak.

- Microsoft Azure Blob depolama birimindeki belgeler bir ortamdan diğerine kopyalanmaz. Bu nedenle, ekli tüm belge ve şablonlar kopyalanmayacak ve kaynak ortamda kalır.

- Yönetici kullanıcı dışındaki tüm kullanıcı hesapları ve iç hizmet kullanıcıları devre dışı bırakılacak. Bu nedenle, Yönetici kullanıcısı, diğer kullanıcıların sisteme geri dönebilmesi için verileri silebilir veya karartırabilir.

- Yönetici kullanıcının, belirli hizmetlere veya URL'lere tümleştirme son noktalarına yeniden bağlanması gibi gerekli yapılandırma değişikliklerini yapması gerekir.

## <a name="copy-the-human-resources-database"></a>İnsan Kaynakları veritabanını Kopyala

Bu görevi tamamlamak için, önce bir örneği kopyalayın ve sonra PowerApps ortamınızı kopyalamak için Microsoft Power Platform Yönetim Merkezi'ne oturum açın.

> [!WARNING]
> Bir örneği kopyaladığınızda, hedef örnekte veritabanı silinir. Hedef örneği bu işlem sırasında kullanılamaz.

1. LCS'de oturum açın ve kopyalamak istediğiniz örneği içeren LCS projesini seçin.

2. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.

3. Kopyalanacak örneği seçin ve sonra **Kopyala**'yı seçin.

4. **Örneği kopyala** görev bölmesinde, üzerine yazılacak örneği seçin ve sonra **Kopyala**'yı seçin. **Kopyalama durumu** alanı değerinin **tamamlandı** olarak güncelleştirilmesini bekleyin.

   ![[Üzerine yazılacak örneği Seç](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. **Power Platform**'u seçin ve Microsoft Power Platform Yönetim Merkezi'nde oturum açın.

   ![[Power Platform öğesini seçin.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Kopyalanacak PowerApps ortamını seçin ve sonra **Kopyala**'yı seçin.

7. Kopyalama işlemi tamamlandığında, hedef örneğe oturum açın ve Common Data Service tümleştirmeyi etkinleştirin. Daha fazla bilgi ve talimatlar için bkz. [Common Data Service entegrasyonunu yapılandırma](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Veri öğeleri ve durumlar

Bir İnsan Kaynakları örneğini kopyaladığınızda aşağıdaki veri öğeleri kopyalanmaz:

- **LogisticsElectronicAddress** tablosundaki e-posta adresleri

- **BatchJobHistory**, **BatchHistory** ve **BatchConstraintHistory** tablolarındaki toplu iş geçmişi

- **SysEmailSMTPPassword** tablosundaki Basit Posta Aktarım Protokolü (SMTP) parolası

- **SysEmailParameters** tablosundaki SMTP geçiş sunucusu

- **PrintMgmtSettings** ve **PrintMgmtDocInstance** tablolarındaki yazdırma yönetimi ayarlar

- **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ve **BatchServerGroup** tablolarındaki ortama özel kayıtlar

- DocuValue tablosundaki Belge ekleri. Bu ekler, kaynak ortamda üzerine yazılmış tüm Microsoft Office şablonları içerir

- **PersonnelIntegrationConfiguration** tablosundaki bağlantı dizesi

Ortama özel oldukları için bu öğelerden bazıları kopyalanmıyor. **BatchServerConfig** ve **SysCorpNetPrinters** kayıtlarını örnekler içerir. Destek biletlerinin hacmi nedeniyle diğer öğeler kopyalanmıyor. Örneğin, SMTP kullanıcı kabul testi (korumalı alan) ortamında hala etkin olduğu için, yinelenen e-postalar gönderilebilir, toplu işler hala etkin olduğundan geçersiz tümleştirme iletileri gönderilebilir ve yöneticilerin yenileme sonrası temizleme eylemleri gerçekleştirebilmesi için kullanıcılar etkinleştirilebilir.

Ayrıca, bir örneği kopyaladığınızda aşağıdaki durumlar da değişecektir:

- Yönetici dışındaki tüm kullanıcılar **devre dışı** olarak ayarlandı.

- Bazı sistem işleri hariç, tüm toplu işler **stopaj** olarak ayarlanmıştır.

## <a name="environment-admin"></a>Ortam yöneticisi

Yöneticiler dahil olmak üzere hedef korumalı alan ortamındaki tüm kullanıcılar yerine kaynak ortam kullanıcıları tarafından değiştirilir. Bir örneği kopyalamadan önce, hedef ortamda bir yönetici olduğunuzdan emin olun. Değilseniz, kopyalama işlemi tamamlandıktan sonra hedef sanal alanı ortamında oturum açamazsınız.

Hedef korumalı alan ortamındaki yönetici olmayan tüm kullanıcılar, korumalı alan ortamında istenmeyen oturum açma yapılmasını engelleyecek şekilde devre dışı bırakılmıştır. Yöneticiler gerektiğinde kullanıcıları yeniden değiştirebilir.
