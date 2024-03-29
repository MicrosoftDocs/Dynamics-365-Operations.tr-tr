---
title: Örnek kopyala
description: Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20a2ffb44f9b99800146e3365e6f0d6df8e9a75e
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324275"
---
# <a name="copy-an-instance"></a>Örnek kopyala

_**Uygulandığı Öğe** tek başına çalışan altyapıda İnsan Kaynakları_ 

> [!NOTE]
> Haziran 2022'den başlayarak İnsan Kaynakları ortamları yalnızca finans ve operasyon uygulama altyapısı üzerinden dağıtılabilir. Daha fazla bilgi için bkz. [Finans ve operasyon altyapısında İnsan Kaynakları sağlama](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finans ve operasyon altyapısı bir kopya örneği işlevini desteklemiyor. Yeni ortamlar dağıtabilir ve veritabanı hareketlerini, kopyalar oluşturmak için kullanabilirsiniz. Personel self servis dağıtımları hakkında daha fazla bilgi için bkz. [Self servisi dağıtımına genel bakış](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Finans ve operasyon altyapısında veritabanı taşımaları hakkında daha fazla bilgi için bkz. [Veritabanı taşıma operasyonu ana sayfası](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz. Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz.

Örneği kopyalamak için aşağıdaki ipuçlarını göz önünde bulundurun:

- Üzerine yazmak istediğiniz İnsan Kaynakları örneği bir korumalı alan ortamı olmalıdır.

- Kopyalama kaynağı ve hedef ortamlar aynı bölgede olmalıdır. Bölgeler arasında kopyalama yapamazsınız.

- Örneği kopyaladıktan sonra oturum açmak için hedef ortamda bir yönetici olmanız gerekir.

- İnsan Kaynakları veritabanını kopyaladığınızda, bir Microsoft Power Apps ortamda bulunan öğeleri (uygulamalar veya veriler) kopyalamayın. Bir Power Apps ortamdaki öğelerin nasıl kopyalanacağı hakkında bilgi için bkz. [Ortam kopyalama](/power-platform/admin/copy-environment). Üzerine yazmak istediğiniz Power Apps ortamı bir korumalı alan ortamı olmalıdır. Power Apps üretim ortamını korumalı alan ortamına dönüştürmek için genel bir kiracı yöneticisi olmanız gerekir. Power Apps ortamın değiştirilmesi hakkında daha fazla bilgi için bkz. [Örneği değiştirme](/dynamics365/admin/switch-instance).

- Örneği korumalı alan ortamınıza kopyalayıp sandbox ortamınızı Dataverse ile birleştirmek isterseniz Dataverse tablolarına özel alanları yeniden uygulamanız gerekir. [Özel alanları Dataverse'e uygulama](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service) konusuna bakın.

## <a name="effects-of-copying-a-human-resources-database"></a>İnsan Kaynakları veritabanını kopyalama etkileri

> [!Note]
> Ağustos 2022'den itibaren Microsoft Azure Blob depolamadaki Belgeler bir üretim ortamı korumalı alan ortamına kopyalanırken dahil edilecektir. Ekli tüm belge ve şablonlar kaynak ortamdan hedef ortama kopyalanacaktır.

Bir İnsan Kaynakları veritabanını kopyaladığınızda aşağıdaki olaylar oluşur:

- Kopyalama işlemi hedef ortamdaki varolan veritabanını siler. Kopyalama işlemi tamamlandıktan sonra, varolan veritabanını kurtaramazsınız.

- Kopyalama işlemi tamamlanana kadar hedef ortam kullanılamayacak.

- "Sistem Yöneticisi" güvenlik rolüne ve diğer iç hizmet kullanıcı hesaplarına sahip olanlar haricindeki tüm kullanıcılar kullanılamaz. Yönetici kullanıcı, diğer kullanıcılar sisteme geri dönmeden önce verileri silebilir.

- "Sistem Yöneticisi" güvenlik rolüne sahip kullanıcılar, tümleştirme uç noktalarını belirli hizmetlere veya URL'lere yeniden bağlama gibi gerekli yapılandırma değişikliklerini yapmalıdır.

## <a name="copy-the-human-resources-database"></a>İnsan Kaynakları veritabanını Kopyala

Bu görevi tamamlamak için, önce bir örneği kopyalayın ve sonra Power Apps ortamınızı kopyalamak için Microsoft Power Platform Yönetim Merkezi'ne oturum açın.

> [!WARNING]
> Bir örneği kopyaladığınızda, hedef örnekte veritabanı silinir. Hedef örneği bu işlem sırasında kullanılamaz.

1. LCS'de oturum açın ve kopyalamak istediğiniz örneği içeren LCS projesini seçin.

2. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.

3. Kopyalanacak örneği seçin ve sonra **Kopyala**'yı seçin.

4. **Örneği kopyala** görev bölmesinde, üzerine yazılacak örneği seçin ve sonra **Kopyala**'yı seçin. **Kopyalama durumu** alanı için **Tamamlandı** olarak güncelleştirilmesini bekleyin.

   ![[Üzerine yazılacak örneği seçin.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. **Power Platform**'u seçin ve Microsoft Power Platform Yönetim Merkezi'nde oturum açın.

   ![[Power Platform'u seçin.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Kopyalanacak Power Apps ortamını seçin ve sonra **Kopyala**'yı seçin.

Power Apps ortamları kopyalama hakkında daha fazla bilgi için bkz. [Bir ortam kopyala](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Kopyalama işlemi tamamlandığında, hedef örneğe oturum açın ve Dataverse tümleştirmeyi etkinleştirin. Daha fazla bilgi ve talimatlar için bkz. [Dataverse entegrasyonunu yapılandırma](./hr-admin-integration-common-data-service.md).

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

Ortama özel oldukları için bu öğelerden bazıları kopyalanmaz. **BatchServerConfig** ve **SysCorpNetPrinters** kayıtlarını örnekler içerir. Destek biletlerinin hacmi nedeniyle diğer öğeler kopyalanmıyor. Örneğin:

- SMTP, kullanıcı kabul test (korumalı alan) ortamında hala etkin olduğundan yinelenen e-postalar gönderilebilir.

- Toplu işler hala etkin olduğundan geçersiz tümleştirme iletileri gönderilebilir.

- Yöneticiler yenileme sonrası temizleme eylemlerini gerçekleştiremeden kullanıcılar etkinleştirilebilir.

Bir örneği kopyaladığınızda aşağıdaki durumlar da değişir:

- "Sistem Yöneticisi" güvenlik rolüne sahip olanlar haricindeki tüm kullanıcılar **Devre Dışı** olarak ayarlanır.

- Bazı sistem işleri hariç, tüm toplu işler **stopaj** olarak ayarlanmıştır.

## <a name="environment-admin"></a>Ortam yöneticisi

Yöneticiler dahil olmak üzere hedef korumalı alan ortamındaki tüm kullanıcılar yerine kaynak ortam kullanıcıları tarafından değiştirilir. Bir kurulumu kopyalamadan önce, kaynak ortamda bir yönetici olduğunuzdan emin olun. Değilseniz kopyalama işleminin tamamlanmasından sonra hedef korumalı alan ortamında oturum açamazsınız.

Hedef korumalı alan ortamındaki yönetici olmayan tüm kullanıcılar, korumalı alan ortamında istenmeyen oturum açma yapılmasını engelleyecek şekilde devre dışı bırakılmıştır. Yöneticiler gerektiğinde kullanıcıları yeniden değiştirebilir.

## <a name="apply-custom-fields-to-dataverse"></a>Özel alanları Dataverse'e uygulama

Örneği korumalı alan ortamınıza kopyalayıp sandbox ortamınızı Dataverse ile birleştirmek isterseniz Dataverse tablolarına özel alanları yeniden uygulamanız gerekir.

Dataverse tablolarına gösterilen her özel alan için aşağıdaki adımları uygulayın:

1. Özel alana gidip **Düzenle**'yi seçin.

2. Özel alanın etkin olduğu her cdm_* varlığı için **Etkin** alanının seçimini kaldırın.

3. **Değişiklikleri Uygula**'yı seçin.

4. Yeniden **Düzenle**'yi seçin.

5. Özel alanın etkin olduğu her cdm_* varlığı için **Etkin** alanını seçin.

6. Yeniden **Değişiklikleri Uygula**'yı seçin.

Seçimi kaldırma, değişiklikleri uygulama, yeniden seçme ve değişiklikleri yeniden uygulama, şemanın Dataverse'i güncelleştirerek özel alanları eklemesini sağlar.

Özel alanlar hakkında daha fazla bilgi için bkz. [Özel alanlar oluşturma ve bunlarla çalışma](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'ı hazırlama](hr-admin-setup-provision.md)</br>
[Örneği kaldırma](hr-admin-setup-remove-instance.md)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
