maps were  created using google fusion tables 

correlation matrix of ditrict location data 
```{r}
district<-read.csv(“placedistrictopendata.csv”)
library(corrplot)
COR<-cor(district)
 corrplot(COR, order="AOE", method="circle", tl.pos="lt", type="upper",        
                  tl.col="black", tl.cex=0.6, tl.srt=45, 
                  addCoef.col="black", addCoefasPercent = TRUE,
                  sig.level=0.50, insig = "black")
  ```
  ##correlation matrix of AFCARS Adoption data
 ```{r}     
    adoptaf<-read.csv(“afcarsadopt.csv”)
COR<-cor(adopaf)
 corrplot(COR, order="AOE", method="circle", tl.pos="lt", type="upper",        
                  tl.col="black", tl.cex=0.6, tl.srt=45, 
                  addCoef.col="black", addCoefasPercent = TRUE,
                  sig.level=0.50, insig = "blank")
  ```

## correlation matrix of AFCARS Foster data 
 
     
 ```{r} 
fosteraf<-read.csv(“afcarsfoster.csv”)
COR<-cor(fosteraf)
 corrplot(COR, order="AOE", method="circle", tl.pos="lt", type="upper",        
                  tl.col="black", tl.cex=0.6, tl.srt=45, 
                  addCoef.col="black", addCoefasPercent = TRUE,
                  sig.level=0.50, insig = "blank")
 ```
 ## correlation matrix of NYTD Service data 
 ```{r} 
nytdserv<-read.csv(“service.csv”)
COR<-cor(nytdserv)
 corrplot(COR, order="AOE", method="circle", tl.pos="lt", type="upper",        
                  tl.col="black", tl.cex=0.6, tl.srt=45, 
                  addCoef.col="black", addCoefasPercent = TRUE,
                  sig.level=0.50, insig = "blank")
  ```
##correlation matrix nytd outcome data 
 ```{r} 
nytdoutcome<-read.csv(“outcome.csv”)
COR<-cor(nytdoutcome)
 corrplot(COR, order="AOE", method="circle", tl.pos="lt", type="upper",        
                  tl.col="black", tl.cex=0.6, tl.srt=45, 
                  addCoef.col="black", addCoefasPercent = TRUE,
                  sig.level=0.50, insig = "blank")
 ```
## logistic regression predicting goal of adoption 
```{r} 
fit <- glm(foster$goaladoption ~ ., data=foster )
 summary(fit)
 ```
                  
 
