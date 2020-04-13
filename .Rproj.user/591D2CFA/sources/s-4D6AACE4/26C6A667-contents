#
# This is the user-interface definition of a Shiny web application. You can
# run the application by clicking 'Run App' above.
#
# Find out more about building applications with Shiny here:
#
#    http://shiny.rstudio.com/
#
library(ggplot2)
library(plotly)
library(shiny)

# Define UI for application that draws a histogram
shinyUI(fluidPage(

    # Application title
    titlePanel("SIR Modeling of Covid19 in Malaysia"),

    sidebarLayout(
        
        sidebarPanel(
            h4("Contributors:"),
            p("Chan Weng Howe (UTM), Wan Nor Arifin (USM)"),
            p(HTML("<br/>")),
            width="3",
            sliderInput("N",
                        "% of Susceptible:",
                        min = 1,
                        max = 100,
                        value = 70),
            sliderInput("betaInit",
                        "Initial contact rate (beta):",
                        min = round(1/14,4),
                        max = round(1,4),
                        value = round(1/8,4)),
            uiOutput("gammaSlider"),
            numericInput('gammaUpper',
                      'Upper Limit of recovery days:',
                      value = 11)
        ),

        # Show a plot of the generated distribution

        mainPanel(
            plotOutput("sirplot")
        )
    )
))
