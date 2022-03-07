---
title: Commerce kanalları için mali tümleştirmeyi ayarlama
description: Bu konu, mali tümleştirme işlevini Commerce kanalları için ayarlama hakkında yönergeler sağlar.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b221bfede5d1db8d7970e1efede85e8dba7fe017
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416306"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce kanalları için mali tümleştirmeyi ayarlama

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Giriş

Bu konu, mali tümleştirme işlevini Commerce kanalları için ayarlama hakkında yönergeler sağlar. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirme genel bakışı](fiscal-integration-for-retail-channel.md).

Mali tümleştirme Kurulumu işlemi aşağıdaki görevleri içerir:

1. Mali aygıt veya mali yazıcı gibi mali kayıt amacıyla kullanılan hizmetleri gösteren mali yapılandırma.
2. Mali aygıt veya hizmetler tarafından mali bağlayıcı kaydedilecek mali belgelerin belge sağlayıcılarını yapılandırın.
3. Mali kayıt işlemi tanımlayan mali kayıt adımları ve mali bağlayıcı ve her adım için kullanılan sağlayıcıları mali belge sırasını yapılandır.
4. Mali kayıt işlemini satış noktası (POS) işlev profillerine atayın.
5. Donanım profilleri için bağlayıcı teknik profilleri atayın.

## <a name="set-up-a-fiscal-registration-process"></a>Mali kayıt işlemi ayarlamak

Mali tümleştirme işlevini kullanmadan önce aşağıdaki ayarları yapılandırmalısınız.

1. Commerce Parametrelerini güncelleyin.

    1. **Commerce paylaşılan parametreler** sayfasında, **Genel** sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın. **Numara serileri** sekmesinde, aşağıdaki referanslar için numara serilerini tanımlayın:

        - Mali teknik profil numarası
        - Mali bağlayıcı grubu numarası
        - Kayıt işlemi numarası

    2. **Commerce parametreleri** sayfasında, mali işlevsel profil numarası için numara serilerini tanımlayın.

    > [!NOTE]
    > Numara serileri isteğe bağlıdır. Tüm mali tümleştirme varlıkları için numaralar, numara serilerinden veya el ile tanımlanabilir.

2. Mali bağlayıcılar ve mali belge sağlayıcıları.

    Bir mali belge sağlayıcısı, işlemlerini temsil eden mali belgeleri ve POS içerisinde, mali cihaz veya servis ile etkileşimde kullanılan kayıtları oluşturmaktan sorumludur. Örneğin, bir mali belge sağlayıcı XML biçiminde bir mali giriş gösterimi oluşturabilir.

    Bir mali cihaz veya hizmeti ile iletişim için mali bağlayıcı sorumludur. Örneğin, bir mali bağlayıcı, bir mali belge sağlayıcısının XML biçiminde oluşturudğu bir mali girişi, bir mali yazıcıya gönderebilir. Mali tümleştirme bileşenleri hakkında daha fazla bilgi için bkz. [Mali cihazlar için mali kayıt işlemi ve mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. **Mali bağlayıcılar** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**), mali tümleştirme amacıyla kullanmayı planladığınız her bir cihaz veya servis için bir XML yapılandırması karşıya yükleyin.

        > [!TIP]
        > **Görünüm**'ü seçerek, geçerli mali bağlayıcı ile ilişkili tüm işlevleri ve teknik profilleri görebilirsiniz.

    2. **Mali belge sağlayıcıları** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**), kullanmayı planladığınız her bir cihaz veya servis için bir XML yapılandırması karşıya yükleyin.

        > [!TIP]
        > **Görünüm**'ü seçerek, geçerli mali belge sağlayıcı ile ilişkili tüm işlev profillerini görebilirsiniz.

    Mali bağlayıcıların ve mali belge sağlayıcıların yapılandırma örnekleri için bkz. [Retail SDK'daki mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Veri eşleme mali belge sağlayıcının parçası olarak kabul edilir. Aynı bağlayıcı için farklı veri eşlemeleri (mesela özel durum düzenlemeleri), farklı mali belge sağlayıcıları oluşturmanız gerekir.

3. Bağlayıcı işlev profilleri ve bağlayıcı teknik profilleri oluşturun.

    1. **Bağlayıcı işlev profilleri** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı fonksiyonel profilleri**), bu mali bağlayıcıyla ilişkili bir mali bağlayıcı ve mali belge sağlayıcısının her bir kombinasyonu için bir bağlayıcı işlev profili oluşturun.

        1. Bir bağlayıcı adı seçin.
        2. Bir belge sağlayıcı seçin.

        Bir bağlayıcı işlev profilinde veri eşleme parametrelerini değiştirebilirsiniz. Mali belge sağlayıcı yapılandırmasındaki varsayılan parametreleri geri yüklemek için **Güncelleştir**'i seçin.

        **Örnekler**

        |   | Biçim | Örnek |
        |---|--------|---------|
        | **KDV oranı ayarları** | değer: VATrate | 1 : 2000, 2 : 1800 |
        | **KDV kodları eşlemesi** | VATcode : değer | vat20: 1, vat18: 2 |
        | **Ödeme türleri eşlemesi** | TenderType : değer | Nakit: 1, Kart: 2 |

        > [!NOTE]
        > Bağlayıcı işlev profilleri şirkete özeldir. Bir mali bağlayıcı ve mali belge sağlayıcısının kombinasyonunu farklı şirketlerde kullanmayı planlıyorsanız, her şirket için bir bağlayıcı işlev profili oluşturmalısınız.

    2. **Bağlayıcı teknik profilleri** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**), her bir mali bağlayıcı için bir bağlayıcı teknik profili oluşturun.

        1. Bir bağlayıcı adı seçin.
        2. Bir bağlayıcı türü seçin. Bir Donanım istasyonuna bağlı cihazlar için **Yerel**'i seçin.

            > [!NOTE]
            > Yalnızca yerel bağlayıcı desteklenmektedir.

        Bir bağlayıcı teknik profilindeki **Cihaz** ve **Ayarlar** sekmesindeki parametreler değiştirilebilir. Mali bağlayıcı yapılandırmasındaki varsayılan parametreleri geri yüklemek için **Güncelleştir**'i seçin. XML yapılandırmasının yeni sürümü yüklenirken, halihazırda kullanımda olan geçerli mali bağlayıcı veya mali belge sağlayıcıyı belirten bir ileti alırsınız. Bu yordam daha önce bir bağlayıcı işlev profili ve bağlayıcı teknik profillerinde el ile yapılmış olan değişiklikleri geçersiz kılmaz. Yeni bir yapılandırmadan varsayılan parametreler kümesini uygulamak için **Bağlayıcı işlev profilleri** sayfası veya **Bağlayıcı teknik profilleri** sayfasında **Güncelleştir**'i seçin.

4. Mali bağlayıcı grupları oluşturun.

    Bir mali bağlayıcı grubu, aynı işlevleri gerçekleştiren ve mali kayıt işleminin aynı adımında kullanılan mali bağlayıcıların fonksiyonel profillerini birleştirir. Örneğin, çok sayıda mali yazıcı modeli bir mağazasında kullanılabiliyorsa, bu mali yazıcılar için mali bağlayıcılar bir mali bağlayıcı grubunda birleştirilebilir.

    1. **Mali bağlayıcı grubu** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı gruplar**), yeni bir mali bağlayıcı grubu oluşturun.
    2. Konnektör grubuna işlevsel profiller ekleyin. **İşlev profilleri** sekmesinde, **Ekle**'yi seçin ve bir profil numarası seçin. Bir mali bağlayıcı grubundaki her bir mali bağlayıcı yalnızca bir fonksiyonel profile sahip olabilir.
    3. Fonksiyonel profilinin kullanımını durdurmak için **Devre dışı bırak** seçeneğini **Evet** olarak seçin. Bu değişiklik yalnızca geçerli bağlayıcı grubu etkiler. Bağlayıcı başka gruplarda aynı işlev profili kullanmak için devam edebilirsiniz.

5. Bir mali kayıt işlemi oluşturun.

    Bir mali kayıt işlemi, kayıt adımlarının sıralaması ve her bir adım için kullanılacak mali bağlayıcı grubu ile tanımlanır.

    1. **Mali kayıt işlemi** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemi**), mali kaydın her bir benzersiz işlemi için yeni bir kayıt oluşturun.
    2. İşlem için kayıt adımları ekleyin:

        1. **Ekle**'yi seçin.
        2. Bir mali bağlayıcı türü seçin.
        3. **Grup numarası** alanında, uygun bir mali bağlayıcı grubu seçin.

6. Mali kayıt işleminin varlıklarını POS profillerine atayın.

    1. **POS işlevi profilleri** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri**), mali kayıt işlemini bir POS işlev profiline atayın. **Düzenle**'yi seçin ve sonra **Mali kayıt işlemi** sekmesinde, **İşlem numarası** alanında bir işlem seçin.
    2. **POS donanım profili** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**), bağlayıcı teknik profillerini bir donanım profiline atayın. **Düzenle**'yi seçin, bir satırı **Mali çevre birimleri** sekmesinde ekleyin, daha sonra **Profil numarası** alanında, bir bağlayıcı teknik profilini seçin.

    > [!NOTE]
    > Çok sayıda teknik profilleri, aynı donanım profiline ekleyebilirsiniz. Ancak, bir donanım profili veya POS işlevi profili herhangi bir mali bağlayıcı grubuyla yalnızca bir kesişime sahip olmalıdır.

    Mali kayıt akışı mali kayıt işlemi ve mali tümleştirme bileşenlerinin bazı parametreleri tarafından tanımlanır: mali belge sağlayıcı için Ticaret yürütme eklentisi ve mali bağlayıcı için Donanım istasyonu eklentisi.

    - Mali kayıt için etkinlik ve hareketlerin aboneliği mali belge sağlayıcısında önceden tanımlanmıştır.
    - Mali belge sağlayıcısı, mali kayıt için kullanılan mali bağlayıcıları tanımlamaktan sorumludur. Mali kayıt işleminin geçerli adımı için bağlayıcı teknik profili ile POS'un eşleştirilmiş olduğu Donanım istasyonunun belirtilmiş olan bağlayıcı işlev profillerine Mali bağlayıcı için eşleşir.
    - Mali belge sağlayıcısı, mali belge sağlayıcı yapılandırmasından veri eşleştirme ayarlarını kullanarak hareket/etkinlik verisini, örn. vergiler ve ödemeler gibi bilgileri bir mali belge oluşturulduğunda kullanır.
    - Mali belge sağlayıcısı bir mali belge oluşturduğunda, mali belge bunu olduğu gibi mali cihaza gönderebilir veya bunu ayrıştırıp ve sonra cihaz uygulama programlama arabirimi (API) komut sırasına dönüştürebilir, iletişimin nasıl ele alındığına bağlı olarak.

7. **Mali kayıt işlemi** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemi**), mali kayıt işlemini doğrulamak için **Doğrula**'yı seçin.

    Aşağıdaki durumlarda, bu tür doğrulama çalıştırmanız önerilir:

    - Yeni kayıt işlemi için tüm ayarları tamamladıktan sonra, kayıt işlemlerini POS işlev profillerine ve donanım profillerine atadığınızda da dahil olmak üzere.
    - Mevcut bir mali kayıt işleminde değişiklik yaptıktan ve bu değişiklikler farklı mali bağlayıcının çalışma zamanında seçilmesine neden olabildikten sonra (örneğin, bir mali kayıt işlemi adımı için bağlayıcı grubu değiştirdiğinizde, bir bağlayıcı grubundaki bağlayıcı işlev profilini etkinleştirin veya yeni bir bağlayıcı işlev profilini bir bağlayıcı grubuna ekleyin).
    - Bağlayıcı teknik profillerin donanım profillerine atamasında değişiklikler yaptıktan sonra.

8. **Dağıtım zamanlaması** sayfasında, **1070** ve **1090** işlerini veriyi kanal veritabanına aktarmak için kullanın.

## <a name="set-up-fiscal-texts-for-discounts"></a>İskontolar mali metinleri ayarlama

Bazı durumlarda, bir iskonto uygulandığında özel bir metnin mali giriş üzerine yazdırılması gerekir. İskontolar için mali metinleri **Mali bağlayıcı grubu** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**) üzerinde ayarlayabilirsiniz.

- POS üzerinde uygulanacak el ile iskontolar için POS işlev profili içindeki **Ürün iskontosu** bilgi kodunda bilgi kodu veya bilgi kodu grubu için bir mali metin ayarlamalısınız.

    1. **Mali bağlayıcı grubu** sayfasında, **Mali giriş için metin**'i seçin.
    2. **Bilgi kodları** sekmesinde, **Ekle**'yi seçin ve bir bilgi kodu veya bilgi kodu grubu seçin.
    3. **Bilgi kodu numarası**'nda bir değer seçin.
    4. **Alt kod numarası** alanında, seçilen bilgi kodu için bir alt kodun gerekli olması durumunda bir değer seçin.
    5. **Mali giriş için metin** alnında, mali girişe yazdırılacak bir mali metin belirleyin.
    6. **Kullanıcı girişini mali girişe yazdır** seçeneğini **Evet** olarak ayarlayarak mali girişteki metnin kullanıcının POS'ta yazdığı metin ile geçersiz kılınmasını sağlayın. Bu seçenek yalnızca **Metin** giriş türüne sahip bilgi kodları için geçerlidir.

    > [!NOTE]
    > Bilgi kodu gruplarının bağlantılı bilgi kodlarının ve tetiklenmiş bilgi kodlarının kullanıldığı senaryoları destekleyen çeşitli bilgi kodlarını belirtebilirsiniz. Bu senaryolarda, mali giriş, iskontonun uygulandığı hareket satırına bağlantılı tüm bilgi kodlarını içeren mali metni içerecektir.

- Kanala özel iskontolarda, iskonto kimliği için bir mali metin tanımlamalısınız.

    1. **Mali bağlayıcı grubu** sayfasında, **Mali giriş için metin**'i seçin.
    2. **İskontolar** sekmesinde, **Ekle**'yi seçin ve bir iskonto kimliği seçin.
    3. **Mali giriş için metin** alnında, mali girişe yazdırılacak bir mali metin belirleyin.

    > [!NOTE]
    > Birden fazla iskonto aynı hareket satırına uygulanıyorsa, mali metin bu iskonto satırıyla bağlantılı tüm mali metinleri içerecektir.

## <a name="set-error-handling-settings"></a>Hata işleme ayarlarını belirleme

Mali tümleştirme içinde kullanılabilen hata işleme seçenekleri, mali kayıt işleminde ayarlanır. Mali tümleştirme içindeki hata işleme hakkında daha fazla bilgi için bkz. [Hata işleme](fiscal-integration-for-retail-channel.md#error-handling).

1. **Mali kayıt işlemi** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemi**) üzerinde, mali kayıt işleminin her bir adımı aşağıdaki parametreleri ayarlayabilirsiniz.

    - **Atlamaya izin ver** – Bu parametre **Atla** seçeneğini hata işleme iletişim kutusuna etkinleştirir.
    - **Kaydedildiği şekilde işaretlemeye izin ver** - Bu parametre **Kaydedildi olarak işaretle** seçeneğini hata işleme iletişim kutusunda etkinleştirir.
    - **Hata durumunda devam** – Bu parametre etkinleştirilmişse, mali kayıt işlemi POS kaydında mali kayıt veya bir hareket veya etkinlik başarısız olursa devam edebilir. Aksi taktirde, bir sonraki kayıt veya etkinliğin mali kaydını yürütmek için operatörün başarısız mali kaydı yeniden denemesi, atlaması veya hareketi veya etkinliği kaydedildi olarak işaretlemesi gerekir. Daha fazla bilgi için bkz [İsteğe bağlı mali kayıt](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > **Hatada devam et** parametresi etkinse, **Atlamaya izin ver** ve **Kaydedildi olarak işaretlenmeye izin ver** parametreleri otomatik olarak devre dışı bırakılır.

2. Hata işleme iletişim kutusundaki **Atla** ve **Kaydedildi olarak işaretle** seçenekleri, **Kaydı atlamaya izin ver veya kaydedildi olarak işaretle** iznine ihtiyaç duyar. Bu nedenle, **İzin grupları** sayfasında (**Retail ve Commerce \> Çalışanlar \> İzin grupları**), **Kaydı atlamaya izin ver veya kaydedildi olarak işaretle** iznini etkinleştirin.
3. **Atla** ve **Kaydedildi olarak işaretle** seçenekleri, operatörlerin mali kayıt başarısız olduğunda ek bilgiler girmesine olanak sağlar. Bu işlevi kullanılabilir kılmak için **Atla** ve **Kaydedildi olarak işaretle** bilgi kodlarını bir mali bağlayıcı grubunda belirtmelisiniz. Operatörlerin girdiği bilgi, mali işleme bağlı bir bilgi kodu hareketi olarak kaydedilir. Bilgi kodları hakkında daha fazla bilgi için bkz. [Bilgi kodları ve bilgi kodu grupları](../info-codes-retail.md).

    > [!NOTE]
    > **Ürün** tetikleme işlevi, mali bağlayıcı gruplarındaki **Atla** ve **Kaydedildi olarak işaretle** için kullanılan bilgi kodlarında desteklenmemektedir.

    - **Mali bağlayıcı grubu** sayfasında, **Bilgi kodları** sekmesinde, bilgi kodlarını veya bilgi kodu gruplarını ve **Atla** ve **Kaydedildi olarak işaretle** alanlarını seçin.

    > [!NOTE]
    > Bir mali belge ve bir mali olmayan belge, mali belge kayıt işleminin herhangi bir sayfasında oluşturulabilir. Bir mali belge sağlayıcısı eklentisi, her tür hareket veya etkinliği mali veya mali olmayan belgelere ilişkili olarak tanımlar. Hata işleme özelliği yalnızca mali belgeler için geçerlidir.
    >
    > - **Mali belge** - Başarıyla kaydedilmesi gereken zorunlu bir belge (örn. bir mali giriş).
    > - **Mali olmayan belge** - Hareket veya etkinlik için destekleyici bir belge (örn. bir hediye kartı fişi).

4. Bir sağlık denetimi hatası ortaya çıktıktan sonra operatörün güncel işlemi işlemeye devam etmesi (örneğin, bir hareketin oluşturulması veya sonlandırılması) için **Sağlık denetimi hatasını atlamaya izin ver** iznini **İzin grupları** sayfasından etkinleştirmeniz gerekir (**Retail ve Commerce \> Personeller \> İzin grupları**). Sağlık denetimi işlemi hakkında daha fazla bilgi için bkz. [Mali kayıt sağlık denetimi](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Mali X/Z raporlarını POS'tan ayarlamak

Mali X/Z raporlarının POS'tan çalıştırılmasını etkinleştirmek için bir POS düzenine yeni düğmeler eklemelisiniz.

- **Düğme kılavuzlar** sayfasında, [Düğme grubu tasarımcısını kullanarak POS düzenlerine POS işlemleri ekleme](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) içindeki talimatları kullanarak tasarımcıyı yükleyin ve bir POS düzenini güncelleştirin.

    1. Güncelleştirilecek düzeni seçin. 
    2. Yeni bir düğme ekleyin ve **Mali x yazdır** düğmesi özelliğini ayarlayın.
    3. Yeni bir düğme ekleyin ve **Mali Z yazdır** düğmesi özelliğini ayarlayın.
    4. **Dağıtım planlayıcısı** sayfasında **1090** işini çalıştırarak değişiklikleri kanal veritabanına aktarın.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Ertelenen mali kaydın el ile yürütülmesini etkinleştir

Ertelenen mali kaydın el ile yürütülmesini etkinleştirmek için POS düzenine yeni bir düğme eklemelisiniz.

- **Düğme kılavuzlar** sayfasında, [Düğme grubu tasarımcısını kullanarak POS düzenlerine POS işlemleri ekleme](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) içindeki talimatları kullanarak tasarımcıyı yükleyin ve bir POS düzenini güncelleştirin.

    1. Güncelleştirilecek düzeni seçin.
    2. Yeni bir düğme ekleyin ve **Mali kayıt işlemini tamamla** düğmesi özelliğini ayarlayın.
    3. **Dağıtım planlayıcısı** sayfasında **1090** işini çalıştırarak değişikliklerinizi kanal veritabanına aktarın.
