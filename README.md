# QR-code-maker-using-Python
# install pillow and qrcodebefore exceution 
# pip install pillow
# pip install qrcode
import qrcode

from qrcode.constants import ERROR_CORRECT_H
from PIL import Image

qr = qrcode.QRCode(
    version=1,
    error_correction=ERROR_CORRECT_H,  
    box_size=10,
    border=5
)

qr.add_data("https://github.com/thekarannagpal/CarRentalSystem")
qr.make(fit=True)

image = qr.make_image(fill_color="black", back_color="white")
image.show()
image.save("github.png")
