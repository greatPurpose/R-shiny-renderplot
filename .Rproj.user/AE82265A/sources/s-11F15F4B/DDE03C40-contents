library(shiny)

ui <- fluidPage(
  titlePanel("BC Liquor Store prices"),
  sidebarLayout(
    sidebarPanel(
      sliderInput("priceInput", "Price", 0, 100, c(25, 40), pre = "$"),
      radioButtons("typeInput", "Product type", choices = c("BEER", "REFRESH"), selected = "BEER"),
      selectInput("countryInput", "Country", choices = c("A", "B", "C"))),
    mainPanel(plotOutput("coolplot"))
    )
)

server <- function(input, output) {
  output$coolplot<-renderPlot({
    plot(rnorm(input$priceInput[1]))})
}

shinyApp(ui = ui, server = server)