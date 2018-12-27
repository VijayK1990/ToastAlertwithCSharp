# ToastAlertwithCSharp
Toast Alert Library written in C# mapping the JavaScript function

Simple Implementation

	protected void BtnShowToast_Click(object sender, EventArgs e)
        {
            ToastType = Convert.ToInt32(DdlToastType.SelectedValue),
                CssClass = DdlToastPosition.SelectedValue,
                Title = TxtToastTitle.Text,
                Message = TxtToastMessage.Text,
                ExtendRules = new ExtendedToastAlertRules()
                {
                    EnableDebugging = false
                }
            };

            Page.ClientScript.RegisterStartupScript(GetType(), 
						JavascriptCodeIdentifier.SHOW_TOAST_ALTER_BAR, ToastAlerter.EmbedToastAlertCodeBlock(Toal), true);
        }
