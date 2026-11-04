export default function handler(req, res) {
  res.setHeader("Content-Type", "application/json");

  if (req.method !== "GET") {
    return res.status(405).json({
      success: false,
      message: "diizinkan"
    });
  }

  return res.status(200).json({
    success: true,
    name: "VIDEOMAX AI",
    backend: "online",
    textToVideo: "terhubung",
    imageToVideo: "terhubung",
    message: "Backend berhasil dijalankan"
  });
}
