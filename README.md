# ORGANIC-PICKLES
"FROM OUR KITCHEN TO YOUR HEART"
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const products = [
  {
    name: "Tomato Sliced Pickle",
    price: "₹120 (200g) / ₹220 (500g)",
    image: "/tomato-pickle.jpg",
  },
  {
    name: "Mix Pickle",
    price: "₹130 (200g) / ₹240 (500g)",
    image: "/mix-pickle.jpg",
  },
  {
    name: "Mango Pickle",
    price: "₹110 (200g) / ₹200 (500g)",
    image: "/mango-pickle.jpg",
  },
];

export default function PickleStore() {
  return (
    <div className="p-4 max-w-4xl mx-auto">
      <h1 className="text-3xl font-bold mb-6 text-center">Organic Pickle</h1>
      <p className="text-center mb-10 italic">Tradition in Every Spoon</p>
      <div className="grid grid-cols-1 sm:grid-cols-3 gap-6">
        {products.map((product, idx) => (
          <Card key={idx} className="rounded-2xl shadow-md">
            <img
              src={product.image}
              alt={product.name}
              className="rounded-t-2xl w-full h-48 object-cover"
            />
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold mb-2">{product.name}</h2>
              <p className="text-sm mb-4">{product.price}</p>
              <Button className="w-full" onClick={() => window.scrollTo({top: document.body.scrollHeight, behavior: 'smooth'})}>Buy Now</Button>
            </CardContent>
          </Card>
        ))}
      </div>

      <div className="mt-20 text-center border-t pt-10">
        <h2 className="text-2xl font-bold mb-4">Scan to Pay</h2>
        <img
          src="/phonepe-qr.jpg"
          alt="PhonePe QR"
          className="mx-auto w-48 h-48 mb-4 border"
        />
        <p className="mb-2">UPI ID: <strong>7811039572@axl</strong></p>
        <p className="text-sm">After payment, send screenshot and address to WhatsApp: 7811039572</p>
      </div>
    </div>

