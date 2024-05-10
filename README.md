# FinalPart2README
Tip Calculator

This project was written for my final of my Advanced Visual Basic Programming class for Spring 2024.
Within this project a user can enter an amount and it will calcualte a tip for 10, 15, 20, and 25 percent. 

Public Class TipCalculator
    Private Sub btnCalculate_Click(sender As Object, e As EventArgs) Handles btnCalculate.Click
        Const tip10perc As Decimal = 0.1
        Const tip15perc As Decimal = 0.15
        Const tip20perc As Decimal = 0.2
        Const tip25perc As Decimal = 0.25

        Dim amount As Decimal
        amount = txtAmount.Text

        If txtAmount.Text = "0" Then
            MessageBox.Show("Please enter an amount greater than zero.", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error)
        End If

        Dim tip10 As Decimal = amount * tip10perc
        Dim total10 As Decimal = amount + tip10

        Dim tip15 As Decimal = amount * tip15perc
        Dim total15 As Decimal = amount + tip15

        Dim tip20 As Decimal = amount * tip20perc
        Dim total20 As Decimal = amount + tip20

        Dim tip25 As Decimal = amount * tip25perc
        Dim total25 As Decimal = amount + tip25


        txtTip10.Text = tip10.ToString("C")
        txtTotal10.Text = total10.ToString("C")

        txtTip15.Text = tip15.ToString("C")
        txtTotal15.Text = total15.ToString("C")

        txtTip20.Text = tip20.ToString("C")
        txtTotal20.Text = total20.ToString("C")

        txtTip25.Text = tip25.ToString("C")
        txtTotal25.Text = total25.ToString("c")



    End Sub
End Class
