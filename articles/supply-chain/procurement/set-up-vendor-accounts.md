---
title: "Satıcı hesaplarını ayarlama"
description: "Bu konu, yeni bir satıcı hesabı oluşturduğunuzda girmeniz gereken bilgilerin türünü açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4a20fca7420e7bd546e29278b40046d69a81aac6
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-vendor-accounts"></a>Satıcı hesaplarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, yeni bir satıcı hesabı oluşturduğunuzda girmeniz gereken bilgilerin türünü açıklar.

Bir satıcı hesabı oluşturduğunuzda, satıcıyla ilgili bilgileri girersiniz. Bu bilgiler belgelere otomatik olarak veri girilmesinde ve satıcı ile ilgili etkinliklerin izlenmesinde kullanılır. Örneğin, bir satıcı için aşağıdaki bilgileri yapılandırabilirsiniz:

-   Bir satıcı grubu atayın. Her satıcının bir satıcı grubuna atanması gerekir. Bir satıcı grubundaki satıcıların ortak olan parametreleri mevcuttur. Örneğin, aynı ödeme koşullarına sahip olabilirler.
-   Katalog içe aktarma için satıcıyı yapılandır. Satıcılar, hizmetlerinin ve öğelerinin kataloğunu içeren bir dosya sağlayabilirler. Bu dosya, çalışanlarınızın satıcıdan sipariş verebilmeleri için karşıya yüklenebilir.
-   Satıcıyı tedarik kategorilerine atayın.
-   Mevcut bir satıcının, kuruluşunuzdaki bir başka tüzel kişilik ile iş yapmasına izin verin.
-   Bir satıcıyı belirli hareket türleri için beklemeye alın.
-   Ödemeleri elektronik olarak gönderebilmek için, satıcı için banka bilgileri ayarlayın.
-   Satıcı için vergi, teslimat, fatura ve ödeme bilgilerini girin. Bu ayarlar satıcı için oluşturduğunuz yeni belgelere varsayılan olarak kopyalanır.
-   Mali hesaplara satıcı ile otomatik olarak hareketleri deftere aktarmak için kullanılan mali boyutları ayarlayın.

Satıcı hesabı oluşturma işlemini hızlandırmak için şablonlar oluşturabilirsiniz. Bir şablon oluşturmak için **Satıcı** sayfasındaki Eylem Bölmesinde, **Seçenekler** &gt; **Kayıt bilgileri**'ne tıklayın. Sonrasında **Şirket hesapları şablonu**'na tıklayın. Şirket hesabı şablonları başka kullanıcılarla paylaşılabilir.  

Ayrıca, kendi kullanımınız için de bir kullanıcı şablonu oluşturabilirsiniz. Örneğin kişiler veya ürünler gibi başka kayıtlarla ilişkilendirilmiş bir satıcıyı silemezsiniz.

## <a name="vendor-account-numbers"></a>Satıcı hesap numaraları
Hesap numarası bir satıcı için benzersiz bir tanımlayıcıdır. Hesap numaralarını, bir satıcı oluşturduğunuzda otomatik olarak oluşturulacak şekilde ayarlayabilirsiniz. Ayrıca, numara serisini, hesap numaralarının el ile girilebilmeleri için yapılandırabilirsiniz. Örneğin, tanımlayıcı olarak satıcının telefon numarasını kullanmak isteyebilirsiniz.

## <a name="vendor-organizations-and-individual-vendors"></a>Satıcı kuruluşları ve tek satıcılar
Yeni bir satıcı hesabı oluşturduğunuzda, satıcının bir organizasyon mu yoksa kişi mi olduğunu seçmeniz gerekir. Seçiminiz satıcı için doldurmanız gereken bilgileri etkiler. Bir kişi için bu bilgiler ad, soyadı ve unvanı içerir. Bir kuruluş için bu bilgiler kuruluş numarası ve çalışanların sayısını içerir.

## <a name="addresses"></a>Adresler
Her bir satıcı için, her biri farklı amaçlar için kullanılacak birden fazla adres tanımlayabilirsiniz. Örneğin, amacı **Fatura** olan bir adres oluşturabilirsiniz. Ya da, eğer satıcıya çek kullanarak ödeme yapacaksanız, **Ödeme alma** amaçlı bir adres ayarlayabilirsiniz. Eğer yabancı bankalarla para transferi için kullanılacak bir adres belirlemeniz gerekiyorsa, amaç **SWIFT** olacaktır.

## <a name="vendor-contacts"></a>Satıcı ilgili kişileri
Bir satıcı için ilgili kişileri kaydedebilirsiniz. Bu kişiler, daha sonra teklifler (RFQs), satınalma siparişleri veya istekleri gibi belgelerde kullanılabilir.  

Bir satıcıyla ilgili kişiler eklemek için **Tüm satıcılar** sayfasında **Satıcı** sekmesindeki **Ayarlama** grubunda, **İlgili Kişiler** &gt; **Kişi ekle**'ye tıklayın.  

Satıcı ilgili kişilerini sıfırdan oluşturabilirsiniz. Alternatif olarak, halihazırda Microsoft Dynamics 365 for Finance and Operations içerisinde kayıtlı bulunan bir başka kişiden ayrıntıları kopyalayabilir ve bilgileri ihtiyaç duyduğunuz şekilde düzenleyebilirsiniz.  

**Not:** Bir satıcı için ilgili kişi eklemek, o satıcı için iletişim bilgisi eklemek ile aynı şey değildir. Bir satıcı için genel iletişim bilgileri ekleyebiliyor olsanız da, söz konusu şirkette iletişim kişisi olan birden fazla şahıs olabilir ve bunların hepsi kendi iletişim bilgilerine sahip olabilirler.  

Bir ilgili kişiye bir belgede başvuruluyorsa, bu ilgili kişi kaydını silemezsiniz. Bunun yerine, ilgili kişiyi devre dışı bırakabilirsiniz.  

Microsoft Office 365'teki kişisel irtibatlarınıza satıcı ilgili kişileri ekleyebilirsiniz. Ancak, önce Finance and Operations ve Office 365 arasında eşitlemeyi, hem Microsoft Exchange Server eşitlemesinde hem de Microsoft Outlook kurulum sihirbazında ayarlamanız gerekir.

## <a name="vendors-in-different-legal-entities"></a>Farklı tüzel kişiliklerdeki satıcılar
Eğer bir satıcı, kuruluşunuz içindeki yalnızca bir tüzel kişilik için kayıtlıysa ve diğer tüm tüzel kişiliklerin de aynı satıcıyı kaydetmesi gerekiyorsa, **Satıcıyı başka bir tüzel varlığa ekle** sayfasını kullanarak, satıcıyı başka tüzel varlıklarla iş yapmak üzere yapılandırabilirsiniz. Seçilmiş tüzel varlık içerisindeki satıcı için satıcı grubu, para birimi ve tutma durumunu seçmelisiniz.  

Kuruluşunuzdaki birden çok tüzel varlık aynı satıcıyla çalışıyorsa ve her tüzel varlık söz konusu satıcı için ayrı bir satıcı hesabı kullanıyorsa, bu satıcı hesaplarının taraf kimliklerini birleştirebilirsiniz. Bu şekilde, adresler ve çalışanların sayısı paylaşılabilir ve böylelikle yalnızca tek bir yerden güncelleştirilmesi gerekir.  

Parti kimliklerini birleştirmek için aşağıdaki adımları izleyin.

1.  **Genel adres defteri** sayfasında, satıcıyı eşlemeye dahil edecek her bir tüzel varlıkta temsil edecek adres defteri kaydını seçin.
2.  Eylem Bölmesinde, **Kayıtları Birleştir**'e tıklayın.

## <a name="agreements"></a>Sözleşmeler
Bir satıcı hesabı ayarladığınızda, bu satıcı ile sahip olduğunuz anlaşmaları da kaydetmek isteyebilirsiniz. Fiyat ve iskonto anlaşmalarını, satıcı kaydı üzerinde eylemler kullanarak ayarlayabilirsiniz. Ayrıca, **Satınalma anlaşması** sayfası üzerinde bir satınalma anlaşması da ayarlayabilirsiniz.

## <a name="putting-a-vendor-on-hold"></a>Bir satıcıyı beklemeye alma
Çeşitli hareket türleri için bir satıcıyı beklemeye alabilirsiniz. Aşağıdaki seçenekler bulunur:

-   **Hayır** – Satıcı üzerinde hiçbir ayrı tutmaya koyulmamıştır.
-   **Fatura** – Satıcı için hiçbir fatura deftere nakledilemez.
-   **Tümü** – Satıcı tüm hareket türleri için beklemeye alınmıştır. Bu hareket türleri satınalma taleplerini, faturaları ve ödemeleri içermektedir.
-   **Ödeme** – Satıcı için hiçbir ödeme oluşturulamaz.
-   **Talep** – Sadece satınalma talepleri oluşturulabilir. Başka hiçbir hareket oluşturulamaz.
-   **Hiçbir zaman** – Satıcı etkin olmadığı için asla beklemeye alınmaz.

Bir satıcıyı beklemeye aldığınızda, bir sebep, tarih ve beklemeye alma durumunun biteceği bir tarih de belirleyebilirsiniz. Bir bitiş tarihi girmezseniz, satıcının beklemede olma durumu sonsuza kadar sürer.

**Satıcı etkinliğini kaldırma** sayfasındaki kritere dayanarak satıcılar için durdurulma durumunu toplu olarak **Tümü**'ne güncelleştirebilir ve bir satıcının durdurulma sebebini girebilirsiniz.

Aşağıdaki ölçütler, bir süre için etkin olmayan satıcıları dahil etmek, personel olan satıcıları dahil etmek veya dışarıda bırakmak ve bir sonraki durdurulma zamanlarından önce yetkisiz bekleme süresinde olan satıcıları dışarıda bırakmak için kullanılır.

- **Satıcı devre dışı bırakma** sayfası üzerindeki **Etkinlik döneminde** alanına girmiş olduğunuz gün sayısına bağlı olarak, uygulama satıcının etkin değil olarak kabul edilmesi için harekete sahip olabileceği son günü hesaplar. Bu, günün tarihi eksi girmiş olduğunuz günlerin sayısıdır. Tarihin hesaplana son tarihten geç olduğu bir satıcı için bir veya daha fazla fatura mevcutsa, satıcı hesap etkinliğini durdurmadan hariç tutulur. Bu ayrıca satıcı bu tarihten sonra ödemelere, açık satınalma taleplerine, açık satınalma siparişlerine, teklif taleplerine veya yanıtlara sahipse de doğrulanır.
- **Bir sonraki durdurmadan önceki yetkisiz kullanım süresi** alanı, en son yetkisiz kullanım tarihini hesaplamak için kullanılır. Bu, günün tarihi eksi girmiş olduğunuz günlerdir. Bu, yalnızca önceden devre dışı bırakılmış satıcılar için geçerlidir. Daha önce devre dışı bırakılmış olma durumunda, uygulama satıcı için diğer devre dışı bırakmaların geçmişini doğrular ve son devre dışı bırakmanın en son ek süreden önce oluşup oluşmadığını kontrol eder. Eğer durum böyleyse, satıcı hesabın etkinliğini kaldırma işlemine dahil edilir.
- **Personelleri dahil et** parametresi, bir personel ile ilişkili olan satıcılar anlamına gelir. Bu personelleri dahil etmek istiyorsanız bunu ayarlayabilirsiniz.

Bu işlem **Satıcı tutma** alanının değerinin **Hiçbir zaman** olduğu satıcıları her zaman dışarıda bırakır.

Doğrulamayı geçen satıcılar beklemeye alınır, bu **Satıcı tutma** alanının değerini **Tümü** ve **Sebep** alanını seçilmiş olana ayarlar. Satıcı için bir beklemede kaydı oluşturulur.

## <a name="vendor-invoice-account"></a>Satıcı fatura hesabı
Birden fazla satıcı aynı fatura adresine sahipse veya bir satıcı bir üçüncü taraf üzerinden faturalandırılıyorsa, satıcı kaydında bir fatura hesabı belirtebilirsiniz. Fatura hesabı, satınalma siparişinden bir satıcı faturası oluşturduğunuzda, fatura tutarının alacaklandırılacağı hesaptır. Eğer satıcı kaydında bir fatura hesabı girmezseniz, satıcı hesabı, fatura hesabı olarak kullanılır.

## <a name="vendor-bank-accounts"></a>Satıcı banka hesapları
Eğer bir satıcı banka hesabına ödeme yapmanız gerekiyorsa, satıcının bankası ve banka hesabı bilgisini **Satıcı banka hesapları** sayfasından girebilirsiniz. Ayrıca banka hesabının ödemeleri ve doğrulaması için bilgileri de girebilirsiniz. Örneğin, satıcı banka hesaplarına provizyonlar ekleyebilirsiniz. Bu provizyonlar daha sonra hesap verisini, örneğin rota numarası ve hesap numaralarının teyit edilmesine kullanılabilir. Satıcıya yapılacak ödemeler için bir varsayılan hesap belirtmeniz gerekir. Ancak, gerçek bir ödeme yaptığınızda, bu hesabı satıcının diğer hesaplarından birine değiştirebilirsiniz.

## <a name="ledger-accounts"></a>Genel muhasebe hesapları
Fatura günlüklerinde otomatik olarak beliren varsayılan hesapları belirtilen satıcı için belirleyebilirsiniz. Bu işlevsellik, zaman içerisinde aynı satıcılardan genellikle aynı türde öğelere ve hizmetlere ödeme yapıyorsanız faydalı olabilir. Varsayılan bir hesap belirttiğinizde, hesap günlüklerine hızlı ve verimli bir şekilde günlük girişleri yapabilirsiniz. Belirttiğiniz varsayılan hesaplar satınalma siparişlerinde veya **Satıcı faturası** üzerinden girilen satıcı faturalarında kullanılmaz.  

Satıcı kaydındaki **Fatura** sekmesinde açabileceğiniz **Varsayılan hesap ayarı** sayfasında varsayılan hesapları seçebilirsiniz. Burada seçtiğiniz hesaplar, bir günlük girdisinde bulunduğunuzda, satıcı için filtrelenmiş hesaplar listesinde görünecektir. Hesaplardan birini varsayılan hesap olarak ayarlayabilirsiniz.




