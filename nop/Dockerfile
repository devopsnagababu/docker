FROM mcr.microsoft.com/dotnet/sdk:7.0
RUN apt update && apt install wget -y && apt install unzip -y
ADD  https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.5/nopCommerce_4.60.5_NoSource_linux_x64.zip /nop/nopCommerce_4.60.5_NoSource_linux_x64.zip
WORKDIR /nop
RUN unzip unzip nopCommerce_4.60.5_NoSource_linux_x64.zip && mkdir bin && mkdir logs
EXPOSE 5000
CMD ["dotnet","Nop.Web.dll","--urls","http://0.0.0.0:5000"]

