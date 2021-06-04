//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;

// Number of seconds.
int seconds = 3666;

//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------


void __fastcall TForm1::Timer1Timer(TObject *Sender)
{
    seconds--;
    int hours, minutes, secondsLocal;
    AnsiString h, min, sec;

    hours = seconds / 3600;
    h = IntToStr(hours);

    minutes = (seconds - hours * 3600) / 60;
    min = IntToStr(minutes);

    secondsLocal = seconds - hours * 3600 - minutes * 60;
    sec = IntToStr(secondsLocal);

    Label1->Caption = h + ":" + min + ":" + sec;

    if (seconds <= 0) {
        Label1->Caption = "End of time";
    }
}
//---------------------------------------------------------------------------
