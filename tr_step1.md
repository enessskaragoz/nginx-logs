###  Seviye: Başlangıç  
  
Bu Senaryoda ilk NGINX API Gateway uygulamanızı dağıtıma çıkartacaksınız ardından log tutma işlemlerini gerçekleştireceksiniz. 

Docker Container Runtime uygulaması kendi uygulama motoru ile Container Paketi haline getirilmiş uygulamaları çalıştırabilmekte ve deploy(dağıtıma çıkarma) operasyonlarını kolaylaştırabilmektedir. Kodlama dünyasında açık kaynak yazılım ekipleri tarafından geliştirilen büyük projeler de artık Docker Image'ları haline getirilip push-to-deploy kavramınca ürüne dönüşmektedirler. Bizler de bu senaryomuzda sizlerle dış dünya tarafından erişime açılabilecek ve dış dünyadan gelen istekleri kendi iç servislerimize yönlendirecek bir İstek Yönlendiricisi (API Gateway) yazıp bu servisi basit Docker komutlarını uygulayarak bir servis haline getireceğiz. Daha sonra bu servisin loglarını tutacağız.  

#### Talimatlar  

Uygulamalarımızı servis eder hale getirmek ve log tutma işlemini gerçekleştirmek için sırasıyla aşağıdaki adımları gerçekleştirmemiz gerekmektedir.    
  
- Docker servisimiz ayakta ve çalışmakta. Şimdi Docker Container Image'ı olan "[Docker NGINX Image](https://hub.docker.com/_/nginx)" uygulamamızı ``docker run --name bb-nginx -d -p 8080:80 nginx:1.22.0-alpine`` komutu ile ayağa kaldıralım.  

- Tebrikler ilk NGINX uygulamanızı çalıştırdınız! Şimdi çalıştırdığınız uygulamanın statü halini kontrol etmeniz için ``docker ps`` diyerek ayakta olan uygulamaları inceleyiniz.  

- Uygulamanızı "bb-nginx" ismine ait bir şekilde listede görüntüleyebiliyorsanız başarıyla uygulamayı ayağa kaldırmış ve hizmet veriyor hale getirmişsiniz demektir.  

- Diyelim ki sayfa görünmüyor, konteynerim neden çalışmıyor öğrenmel için ``docker logs bb-nginx`` diyerek, tüm logları görebilirsiniz.  

- Elbette kapsayıcımızda bir hata yok ve güzel çalışıyor. Buna rağmen çok fazla çıktı var. ``docker logs bb-nginx --tail 5`` diyerek, loglardan son 5 satırı görebilirsiniz.  

- Ya da belki bir saat önce bir şeylerin ters gittiğini düşünüyorsunuz ``docker logs bb-nginx --until=60m`` diyerek, son 1 saat içindeki logları görebilirsiniz.  

- Çalışan uygulamaya erişmek için sağ yukarıda bulunan "Sunucuya Eriş" butonuna tıklayarak uygulamayı ayağa kaldırdığınız port olan "8080" port numarasını girerek servisinize erişebilirsiniz.  

- Tebrikler Nginx uygulamanıza erişebildiniz, dağıtıma(deploy) çıkarttınız ve logların kontrolünü sağladınız.  

Bu eğitimle birlikte Docker ile ilk Nginx uygulamanızı Temel Docker Komutları kullanarak çalıştırdınız HTTP Web Servis uygulamalarının sunucu tarafında nasıl çalıştırılabildiğini incelediniz ve loglarını görüntülediniz.  

Yeni Senaryolarla Öğrenmeye Devam.  







