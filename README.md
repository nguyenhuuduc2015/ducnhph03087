# ducnhph03087
Public Class Form1
    'xu ly su kien click

    Private Sub Label1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Label1.Click

    End Sub

    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
        ' khai bao bien
        Dim hours As Double
        Dim wage As Decimal
        Dim earnings As Decimal

        Const hour_limit As Integer = 40 ' khai bao hang so
        ' gan du lieu cho nguoi dung va nhap vao bien
        hours = Val(TextBox1.Text)
        wage = Val(TextBox2.Text)

        ' xac dinh cach tinh thu nhap
        If hours <= hour_limit Then
            ' neu nho hon hoac bang 40h, tinh luong theo thu lao co ban
            earnings = hours * wage
        Else
            ' neu lon hon 40h, tinh theo tien luong co ban 40h truoc
            earnings = hour_limit * wage
            ' tinh thu lao gap ruoi cho lam them gio
            earnings += (hours - hour_limit) * (1.5 * wage)

        End If
        ' gan ket qua cho label
        TextBox3.Text = String.Format("{0:c}", earnings)
    End Sub 'caculator button click
End Class
