---
title: (RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma
description: Bu makalede, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında dosyayı içeri aktarmak için ER biçiminde yapılandırmayı nasıl tasarlayacağı hakkında bilgiler sağlanmaktadır.
author: kfend
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 5254a3d631129d0e41fcd37a341b54f97cfe6a9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290019"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar. Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir. Başlamadan önce [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'nden IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını indirin.

1.    **Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.
2.    Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.
3.    **Raporlama konfigürasyonları**'na tıklayın.

## <a name="create-a-new-data-model-configuration"></a>Yeni bir veri modeli yapılandırması oluşturun
1.    İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.
2.    **Ad** alanına "XML dosyasını içe aktarma modeli" yazın.
3.    **Konfigürasyon oluştur**'u tıklatın.
4.    **Tasarımcı**'yı tıklatın.
5.    Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.
6.    **Ad** alanına "Kök" yazın.
7.    **Ekle** öğesine tıklayın.
8.    Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.
9.    **Ad** alanına "Liste" yazın.
10.    **Madde türü** alanında **Kayıt listesi**'ni seçin.
11.    **Ekle** öğesine tıklayın.
12.    Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.
13.    **Ad** alanına "Kod" yazın.
14.    **Madde türü** alanında **Dize**'yi seçin.
15.    **Ekle** öğesine tıklayın.
16.    **Kaydet**'e tıklayın.
17.    Sayfayı kapatın.
18.    **Durumu değiştir** öğesine tıklayın.
19.    **Tamamla** öğesine tıklayın.
20.    **Tamam**'a tıklayın.

## <a name="create-a-format-for-data-import"></a>Veri içe aktarma için biçim oluşturma
1.    İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.
2.    **Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.
3.    **Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.
4.    **Veri içe aktarmayı destekler** alanında **Evet**'i seçin.
5.    **Konfigürasyon oluştur**'u tıklatın.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama
1.    **Tasarımcı**'yı tıklatın.
2.    İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.
3.    Ağaçta seçin **XML\Element**.
4.    **Ad** alanına "kök" yazın.
5.    **Tamam**'a tıklayın.
6.    Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.
7.    Ağaçta seçin **XML\Element**.
8.    **Ad** alanına "belge" yazın.
9.    **Çokluluk** alanında **Bir fazla**'yı seçin.
10.    **Tamam**'a tıklayın.
11.    Ağaçta **kök\belge** öğesini seçin.
12.    Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.
13.    Ağaçta seçin **XML\Attribute**.
14.    **Ad** alanına "Kimlik" yazın.
15.    **Tamam**'a tıklayın.
16.    **Kaydet**'e tıklayın.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama
1. **Biçimi modelle eşle**'ye tıklayın.
2. **Yeni**'ye tıklayın.
3. **Tanım** alanına bir değer girin veya buradan bir değer seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Ad** alanına "Eşleme" yazın.
6. **Kaydet**'e tıklayın.
7. **Tasarımcı**'yı tıklatın.
8. Ağaçta, **biçim**'i genişletin.
9. Ağaçta **biçim\root: XML Element(root)**'u genişletin.
10.    Ağaçta **biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin. (belge)**.
11.    **Bağla**'ya tıklayın.
12.    Ağaçta **biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin. (belge)**.
13.    Ağaçta **biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin. (belge)\kimlik**.
14.    Ağaçta **List = format.root.document**'i genişletin.
15.    Ağaçta **List = format.root.document\Code**'u seçin.
16.    **Bağla**'ya tıklayın.
17.    **Kaydet**'e tıklayın.
18.    Sayfayı kapatın.
 
## <a name="run-format-mapping"></a>Biçim eşlemeyi çalıştırın
1. **Çalıştır**'a tıklayın.
2. **Gözat** düğmesine tıklayın ve **ıncomingdocumenttolearnhowtohandleoptionalattributes. xml**'i seçin.
3. **Tamam**'a tıklayın.

> [!NOTE]
> Biçim tasarımı 'belge' öğesi için 'kimlik' özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme
1. Sayfayı kapatın.
2. Ağaçta **kök\belge** öğesini genişletin.
3. Ağaçta **kök\belge\kimlik** öğesini seçin.
4. **Boş öznitelik alanı** alanı için **Evet**'i seçin.
5. **Kaydet**'e tıklayın.
 
## <a name="run-format-mapping-to-test-changes"></a>Test değişikliklerinde biçim eşlemesi çalıştırma
1. **Biçimi modelle eşle**'ye tıklayın.
2. **Çalıştır**'a tıklayın.
3. **Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.
4. **Tamam**'a tıklayın.
5. Oluşturulan dosyayı gözden geçirin. 

> [!NOTE]
> Biçim tasarımı olarak içe aktarılan aynı dosya "belge" öğesi için "kimlik" özniteliğini isteğe bağlı olarak kabul etmektedir.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
