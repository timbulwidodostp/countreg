# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Fitting Count Regression Models with Latent Covariates Use countreg (lavacreg) With (In) R Software
install.packages("lavacreg")
library("lavacreg")
countreg = read.csv("https://raw.githubusercontent.com/timbulwidodostp/countreg/main/countreg/countreg.csv",sep = ";")
# Estimation Fitting Count Regression Models with Latent Covariates Use countreg (lavacreg) With (In) R Software
countreg_1 <- countreg(forml = "dv ~ z11", data = countreg, family = "poisson")
summary(countreg_1)
countreg_2 <- countreg(forml = "dv ~ eta1 + z11 + z21", lv = list(eta1 = c("z41", "z42", "z43")), group = "treat", data = countreg, family = "poisson")
summary(countreg_2)
# Fitting Count Regression Models with Latent Covariates Use countreg (lavacreg) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished